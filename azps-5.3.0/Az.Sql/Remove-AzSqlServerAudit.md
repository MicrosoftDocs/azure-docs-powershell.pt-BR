---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Remove-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerAudit.md
ms.openlocfilehash: ce9bf1a2c7b72e6da92c17e343a993294f8e335d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427901"
---
# <span data-ttu-id="ba606-101">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="ba606-101">Remove-AzSqlServerAudit</span></span>

## <span data-ttu-id="ba606-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ba606-102">SYNOPSIS</span></span>
<span data-ttu-id="ba606-103">Remove as configurações de auditoria de um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="ba606-103">Removes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="ba606-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ba606-104">SYNTAX</span></span>

### <span data-ttu-id="ba606-105">ServerParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ba606-105">ServerParameterSet (Default)</span></span>
```
Remove-AzSqlServerAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba606-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba606-106">ServerObjectParameterSet</span></span>
```
Remove-AzSqlServerAudit -ServerObject <AzureSqlServerModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba606-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ba606-107">DESCRIPTION</span></span>
<span data-ttu-id="ba606-108">O cmdlet **Remove-AzSqlServerAudit** remove as configurações de auditoria de um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="ba606-108">The **Remove-AzSqlServerAudit** cmdlet removes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="ba606-109">Especifique os parâmetros *ResourceGroupName* e *nomedoservidor* para identificar o servidor.</span><span class="sxs-lookup"><span data-stu-id="ba606-109">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="ba606-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ba606-110">EXAMPLES</span></span>

### <span data-ttu-id="ba606-111">Exemplo 1: remover as configurações de auditoria de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="ba606-111">Example 1: Remove the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
```

### <span data-ttu-id="ba606-112">Exemplo 2: remover, por meio de pipeline, as configurações de auditoria de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="ba606-112">Example 2: Remove, through pipeline, the auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Remove-AzSqlServerAudit
```

## <span data-ttu-id="ba606-113">OS</span><span class="sxs-lookup"><span data-stu-id="ba606-113">PARAMETERS</span></span>

### <span data-ttu-id="ba606-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba606-114">-AsJob</span></span>
<span data-ttu-id="ba606-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ba606-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba606-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba606-116">-DefaultProfile</span></span>
<span data-ttu-id="ba606-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ba606-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba606-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba606-118">-ResourceGroupName</span></span>
<span data-ttu-id="ba606-119">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ba606-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba606-120">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="ba606-120">-ServerName</span></span>
<span data-ttu-id="ba606-121">Nome do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ba606-121">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba606-122">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="ba606-122">-ServerObject</span></span>
<span data-ttu-id="ba606-123">O objeto do servidor para gerenciar sua política de auditoria.</span><span class="sxs-lookup"><span data-stu-id="ba606-123">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba606-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ba606-124">-Confirm</span></span>
<span data-ttu-id="ba606-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba606-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba606-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba606-126">-WhatIf</span></span>
<span data-ttu-id="ba606-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ba606-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba606-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ba606-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba606-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba606-129">CommonParameters</span></span>
<span data-ttu-id="ba606-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba606-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba606-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba606-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba606-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ba606-132">INPUTS</span></span>

### <span data-ttu-id="ba606-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ba606-133">System.String</span></span>

### <span data-ttu-id="ba606-134">Microsoft. Azure. Commands. Sql. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="ba606-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="ba606-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ba606-135">OUTPUTS</span></span>

### <span data-ttu-id="ba606-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ba606-136">System.Boolean</span></span>

## <span data-ttu-id="ba606-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ba606-137">NOTES</span></span>

## <span data-ttu-id="ba606-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ba606-138">RELATED LINKS</span></span>
