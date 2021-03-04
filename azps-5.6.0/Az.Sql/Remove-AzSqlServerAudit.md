---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/Remove-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerAudit.md
ms.openlocfilehash: be2017c829a97196ad5cf2cef9d3dbd71144a325
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890977"
---
# <span data-ttu-id="0fd0d-101">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="0fd0d-101">Remove-AzSqlServerAudit</span></span>

## <span data-ttu-id="0fd0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fd0d-102">SYNOPSIS</span></span>
<span data-ttu-id="0fd0d-103">Remove as configurações de auditoria de um servidor SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="0fd0d-103">Removes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="0fd0d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0fd0d-104">SYNTAX</span></span>

### <span data-ttu-id="0fd0d-105">ServerParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0fd0d-105">ServerParameterSet (Default)</span></span>
```
Remove-AzSqlServerAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fd0d-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fd0d-106">ServerObjectParameterSet</span></span>
```
Remove-AzSqlServerAudit -ServerObject <AzureSqlServerModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fd0d-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0fd0d-107">DESCRIPTION</span></span>
<span data-ttu-id="0fd0d-108">O cmdlet **Remove-AzSqlServerAudit** remove as configurações de auditoria de um servidor SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="0fd0d-108">The **Remove-AzSqlServerAudit** cmdlet removes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="0fd0d-109">*Especifique os parâmetros ResourceGroupName* *e ServerName* para identificar o servidor.</span><span class="sxs-lookup"><span data-stu-id="0fd0d-109">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="0fd0d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0fd0d-110">EXAMPLES</span></span>

### <span data-ttu-id="0fd0d-111">Exemplo 1: Remover as configurações de auditoria de um servidor SQL Azure</span><span class="sxs-lookup"><span data-stu-id="0fd0d-111">Example 1: Remove the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
```

### <span data-ttu-id="0fd0d-112">Exemplo 2: Remover, por meio de pipeline, as configurações de auditoria de um servidor SQL Azure</span><span class="sxs-lookup"><span data-stu-id="0fd0d-112">Example 2: Remove, through pipeline, the auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Remove-AzSqlServerAudit
```

## <span data-ttu-id="0fd0d-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0fd0d-113">PARAMETERS</span></span>

### <span data-ttu-id="0fd0d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0fd0d-114">-AsJob</span></span>
<span data-ttu-id="0fd0d-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0fd0d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0fd0d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fd0d-116">-DefaultProfile</span></span>
<span data-ttu-id="0fd0d-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0fd0d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fd0d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fd0d-118">-ResourceGroupName</span></span>
<span data-ttu-id="0fd0d-119">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0fd0d-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="0fd0d-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0fd0d-120">-ServerName</span></span>
<span data-ttu-id="0fd0d-121">SQL nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="0fd0d-121">SQL server name.</span></span>

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

### <span data-ttu-id="0fd0d-122">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="0fd0d-122">-ServerObject</span></span>
<span data-ttu-id="0fd0d-123">O objeto server para gerenciar sua política de auditoria.</span><span class="sxs-lookup"><span data-stu-id="0fd0d-123">The server object to manage its audit policy.</span></span>

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

### <span data-ttu-id="0fd0d-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0fd0d-124">-Confirm</span></span>
<span data-ttu-id="0fd0d-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fd0d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fd0d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fd0d-126">-WhatIf</span></span>
<span data-ttu-id="0fd0d-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0fd0d-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0fd0d-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0fd0d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fd0d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fd0d-129">CommonParameters</span></span>
<span data-ttu-id="0fd0d-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fd0d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fd0d-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0fd0d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fd0d-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0fd0d-132">INPUTS</span></span>

### <span data-ttu-id="0fd0d-133">System.String</span><span class="sxs-lookup"><span data-stu-id="0fd0d-133">System.String</span></span>

### <span data-ttu-id="0fd0d-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="0fd0d-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="0fd0d-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0fd0d-135">OUTPUTS</span></span>

### <span data-ttu-id="0fd0d-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0fd0d-136">System.Boolean</span></span>

## <span data-ttu-id="0fd0d-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="0fd0d-137">NOTES</span></span>

## <span data-ttu-id="0fd0d-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0fd0d-138">RELATED LINKS</span></span>
