---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B5A2F2A8-5D20-47E4-AFC5-44F687142A08
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e40d833125725f0ae1baff920a283112db24cdc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945864"
---
# <span data-ttu-id="5447f-101">Set-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="5447f-101">Set-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="5447f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5447f-102">SYNOPSIS</span></span>
<span data-ttu-id="5447f-103">Modifica as propriedades de um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="5447f-103">Modifies the properties of an Azure SQL Database server.</span></span>

## <span data-ttu-id="5447f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5447f-104">SYNTAX</span></span>

```
Set-AzureSqlDatabaseServer -ServerName <String> -AdminPassword <String> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5447f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5447f-105">DESCRIPTION</span></span>
<span data-ttu-id="5447f-106">O cmdlet **set-AzureSqlDatabaseServer** modifica as propriedades da instância especificada do servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="5447f-106">The **Set-AzureSqlDatabaseServer** cmdlet modifies the properties of the specified instance of Azure SQL Database Server.</span></span>
<span data-ttu-id="5447f-107">Na versão atual, você só pode atualizar a senha da conta de administrador de um servidor.</span><span class="sxs-lookup"><span data-stu-id="5447f-107">In the current release, you can only update the administrator account password for a server.</span></span>

## <span data-ttu-id="5447f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5447f-108">EXAMPLES</span></span>

### <span data-ttu-id="5447f-109">Exemplo 1: alterar a senha de um servidor</span><span class="sxs-lookup"><span data-stu-id="5447f-109">Example 1: Change the password for a server</span></span>
```
PS C:\>Set-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y" -AdminPassword "NewPassword"
```

<span data-ttu-id="5447f-110">Esse comando altera a senha da conta de administrador para o servidor do banco de dados SQL do Azure chamado lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="5447f-110">This command changes the administrator account password for the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="5447f-111">OS</span><span class="sxs-lookup"><span data-stu-id="5447f-111">PARAMETERS</span></span>

### <span data-ttu-id="5447f-112">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="5447f-112">-AdminPassword</span></span>
<span data-ttu-id="5447f-113">Especifica a senha da conta de administrador para o servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="5447f-113">Specifies the administrator account password for the Azure SQL Database server.</span></span>
<span data-ttu-id="5447f-114">Você deve especificar uma senha forte.</span><span class="sxs-lookup"><span data-stu-id="5447f-114">You must specify a strong password.</span></span>
<span data-ttu-id="5447f-115">Para obter mais informações, consulte [senhas de alta segurança](https://go.microsoft.com/fwlink/p/?LinkId=154152) ( https://go.microsoft.com/fwlink/p/?LinkId=154152) na Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="5447f-115">For more information, see [Strong Passwords](https://go.microsoft.com/fwlink/p/?LinkId=154152) (https://go.microsoft.com/fwlink/p/?LinkId=154152) at the Microsoft Developer Network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5447f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="5447f-116">-Force</span></span>
<span data-ttu-id="5447f-117">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="5447f-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5447f-118">-Perfil</span><span class="sxs-lookup"><span data-stu-id="5447f-118">-Profile</span></span>
<span data-ttu-id="5447f-119">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="5447f-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5447f-120">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="5447f-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5447f-121">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="5447f-121">-ServerName</span></span>
<span data-ttu-id="5447f-122">Especifica o nome do servidor que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="5447f-122">Specifies the name of the server that this cmdlet modifies.</span></span>
<span data-ttu-id="5447f-123">Especifique o nome do servidor, não o nome DNS totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="5447f-123">Specify the server name, not the fully qualified DNS name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5447f-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5447f-124">-Confirm</span></span>
<span data-ttu-id="5447f-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5447f-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5447f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5447f-126">-WhatIf</span></span>
<span data-ttu-id="5447f-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5447f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5447f-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5447f-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5447f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5447f-129">CommonParameters</span></span>
<span data-ttu-id="5447f-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5447f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5447f-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5447f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5447f-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5447f-132">INPUTS</span></span>

### <span data-ttu-id="5447f-133">Microsoft. WindowsAzure. Commands. SQLDatabase. Model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="5447f-133">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="5447f-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5447f-134">OUTPUTS</span></span>

## <span data-ttu-id="5447f-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5447f-135">NOTES</span></span>

## <span data-ttu-id="5447f-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5447f-136">RELATED LINKS</span></span>

[<span data-ttu-id="5447f-137">Banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="5447f-137">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="5447f-138">Operações para bancos de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="5447f-138">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="5447f-139">Get-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="5447f-139">Get-AzureSqlDatabaseServer</span></span>](./Get-AzureSqlDatabaseServer.md)

[<span data-ttu-id="5447f-140">New-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="5447f-140">New-AzureSqlDatabaseServer</span></span>](./New-AzureSqlDatabaseServer.md)

[<span data-ttu-id="5447f-141">Remove-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="5447f-141">Remove-AzureSqlDatabaseServer</span></span>](./Remove-AzureSqlDatabaseServer.md)


