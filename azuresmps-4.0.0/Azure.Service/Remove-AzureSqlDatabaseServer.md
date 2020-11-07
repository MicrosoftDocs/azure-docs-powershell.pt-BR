---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F73A078E-F9F2-4520-BF55-DFFE82BE4466
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a8127a77ecfdc5aa36659060cb5469206a9988d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946107"
---
# <span data-ttu-id="5c8d4-101">Remove-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="5c8d4-101">Remove-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="5c8d4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5c8d4-102">SYNOPSIS</span></span>
<span data-ttu-id="5c8d4-103">Remove um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="5c8d4-103">Removes an Azure SQL Database server.</span></span>

## <span data-ttu-id="5c8d4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5c8d4-104">SYNTAX</span></span>

```
Remove-AzureSqlDatabaseServer -ServerName <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5c8d4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5c8d4-105">DESCRIPTION</span></span>
<span data-ttu-id="5c8d4-106">O cmdlet **Remove-AzureSqlDatabaseServer** remove a instância especificada do servidor de banco de dados SQL do Azure da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="5c8d4-106">The **Remove-AzureSqlDatabaseServer** cmdlet removes the specified instance of Azure SQL Database Server from the current subscription.</span></span>
<span data-ttu-id="5c8d4-107">Esse cmdlet exclui todos os bancos de dados no servidor.</span><span class="sxs-lookup"><span data-stu-id="5c8d4-107">This cmdlet deletes all databases on the server.</span></span>

## <span data-ttu-id="5c8d4-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5c8d4-108">EXAMPLES</span></span>

### <span data-ttu-id="5c8d4-109">Exemplo 1: remover um servidor de banco de dados</span><span class="sxs-lookup"><span data-stu-id="5c8d4-109">Example 1: Remove a database server</span></span>
```
PS C:\>Remove-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="5c8d4-110">Esse comando Remove o servidor do banco de dados SQL do Azure chamado lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="5c8d4-110">This command removes the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="5c8d4-111">OS</span><span class="sxs-lookup"><span data-stu-id="5c8d4-111">PARAMETERS</span></span>

### <span data-ttu-id="5c8d4-112">-Force</span><span class="sxs-lookup"><span data-stu-id="5c8d4-112">-Force</span></span>
<span data-ttu-id="5c8d4-113">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="5c8d4-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5c8d4-114">-Perfil</span><span class="sxs-lookup"><span data-stu-id="5c8d4-114">-Profile</span></span>
<span data-ttu-id="5c8d4-115">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="5c8d4-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5c8d4-116">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="5c8d4-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5c8d4-117">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="5c8d4-117">-ServerName</span></span>
<span data-ttu-id="5c8d4-118">Especifica o nome do servidor que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="5c8d4-118">Specifies the name of the server that this cmdlet removes.</span></span>
<span data-ttu-id="5c8d4-119">Especifique o nome do servidor, não o nome DNS totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="5c8d4-119">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="5c8d4-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5c8d4-120">-Confirm</span></span>
<span data-ttu-id="5c8d4-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c8d4-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c8d4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c8d4-122">-WhatIf</span></span>
<span data-ttu-id="5c8d4-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5c8d4-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c8d4-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5c8d4-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c8d4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c8d4-125">CommonParameters</span></span>
<span data-ttu-id="5c8d4-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c8d4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c8d4-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c8d4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c8d4-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5c8d4-128">INPUTS</span></span>

### <span data-ttu-id="5c8d4-129">Microsoft. WindowsAzure. Commands. SQLDatabase. Model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="5c8d4-129">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="5c8d4-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5c8d4-130">OUTPUTS</span></span>

## <span data-ttu-id="5c8d4-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5c8d4-131">NOTES</span></span>

## <span data-ttu-id="5c8d4-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5c8d4-132">RELATED LINKS</span></span>

[<span data-ttu-id="5c8d4-133">Banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="5c8d4-133">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="5c8d4-134">Excluir servidor</span><span class="sxs-lookup"><span data-stu-id="5c8d4-134">Delete Server</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505695.aspx)

[<span data-ttu-id="5c8d4-135">Operações para bancos de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="5c8d4-135">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="5c8d4-136">Get-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="5c8d4-136">Get-AzureSqlDatabaseServer</span></span>](./Get-AzureSqlDatabaseServer.md)

[<span data-ttu-id="5c8d4-137">New-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="5c8d4-137">New-AzureSqlDatabaseServer</span></span>](./New-AzureSqlDatabaseServer.md)

[<span data-ttu-id="5c8d4-138">Set-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="5c8d4-138">Set-AzureSqlDatabaseServer</span></span>](./Set-AzureSqlDatabaseServer.md)


