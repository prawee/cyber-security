# How to make CRUD of User with Prisma

## Required
<https://github.com/prawee/cyber-security/blob/master/how-to-make-admin-with-express.md>

## Create
```bash
app.post('/user', async(req, res) => {
    const response = await prisma.user.create({
        data: {
            username: req.body.username,
            password: req.body.password,
            cardId: req.body.cardId
        }
    })
    if (response) {
        res.json({
            message: 'add data successfully',
        });
    } else {
        res.json({
            message: 'add data error',
        });
    }
    
});
```

## List
```bash
const data = await prisma.user.findMany();
    const data = await prisma.user.findMany();
    const finalData = await data.map(record => {
         delete record.password;
         return record;
    });
    res.json({
        message: 'ok',
        data
    });
```

## Update
```bash
app.put('/user', async(req, res) => {
    const response = await prisma.user.update({
        select: {
            password: true,
            id: true
        },
        where: {
            id: req.body.id
        },
        data: {
            password: req.body.password
        }
    });
    if (response) {
        res.json({
            message: "update sucessfully"
        })
    } else {
        res.json({
            message: 'update is failed'
        })
    }
});
```

## Delete
```bash
app.delete('/user', async(req, res) => {
    const response = await prisma.user.delete({
        where: {
            id: req.body.id
        },
        select: {
            username: true
        }
    });
    if (response) {
        res.json({
            message: "deleted sucessfully"
        })
    } else {
        res.json({
            message: 'delete is failed'
        })
    }
});
```
