---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Remove-AzSqlServerMSSupportAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerMSSupportAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerMSSupportAudit.md
ms.openlocfilehash: 1e9586f6a16562217f4c5d9eb7778ba6ec887a68
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116128"
---
# <span data-ttu-id="cfaa2-101">Remove-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="cfaa2-101">Remove-AzSqlServerMSSupportAudit</span></span>

## <span data-ttu-id="cfaa2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cfaa2-102">SYNOPSIS</span></span>
<span data-ttu-id="cfaa2-103">Remove as configurações de auditoria de operações de suporte da Microsoft de um servidor SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="cfaa2-103">Removes the Microsoft support operations auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="cfaa2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cfaa2-104">SYNTAX</span></span>

### <span data-ttu-id="cfaa2-105">ServerParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cfaa2-105">ServerParameterSet (Default)</span></span>
```
Remove-AzSqlServerMSSupportAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfaa2-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfaa2-106">ServerObjectParameterSet</span></span>
```
Remove-AzSqlServerMSSupportAudit -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfaa2-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="cfaa2-107">DESCRIPTION</span></span>
<span data-ttu-id="cfaa2-108">O cmdlet **Remove-AzSqlServerMSSupportAudit** remove as configurações de auditoria de operações de suporte da Microsoft de um servidor SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="cfaa2-108">The **Remove-AzSqlServerMSSupportAudit** cmdlet removes the  Microsoft support operations auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="cfaa2-109">Para usar o cmdlet, use os parâmetros *ResourceGroupName* e *ServerName* para identificar o servidor.</span><span class="sxs-lookup"><span data-stu-id="cfaa2-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="cfaa2-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cfaa2-110">EXAMPLES</span></span>

### <span data-ttu-id="cfaa2-111">Exemplo 1: Remover as configurações de auditoria de operações de suporte da Microsoft de um servidor SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="cfaa2-111">Example 1: Remove the Microsoft support operations auditing settings of an Azure SQL server</span></span>
```powershell
PS C:\>Remove-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

### <span data-ttu-id="cfaa2-112">Exemplo 2: Remover, por meio de pipeline, as configurações de auditoria de suporte da Microsoft de um servidor SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="cfaa2-112">Example 2: Remove, through pipeline, the Microsoft support auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Remove-AzSqlServerMSSupportAudit
```

## <span data-ttu-id="cfaa2-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cfaa2-113">PARAMETERS</span></span>

### <span data-ttu-id="cfaa2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cfaa2-114">-AsJob</span></span>
<span data-ttu-id="cfaa2-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="cfaa2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cfaa2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfaa2-116">-DefaultProfile</span></span>
<span data-ttu-id="cfaa2-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cfaa2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfaa2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfaa2-118">-ResourceGroupName</span></span>
<span data-ttu-id="cfaa2-119">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cfaa2-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="cfaa2-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cfaa2-120">-ServerName</span></span>
<span data-ttu-id="cfaa2-121">Nome do servidor SQL.</span><span class="sxs-lookup"><span data-stu-id="cfaa2-121">SQL server name.</span></span>

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

### <span data-ttu-id="cfaa2-122">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="cfaa2-122">-ServerObject</span></span>
<span data-ttu-id="cfaa2-123">O objeto do servidor para gerenciar sua política de auditoria.</span><span class="sxs-lookup"><span data-stu-id="cfaa2-123">The server object to manage its audit policy.</span></span>

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

### <span data-ttu-id="cfaa2-124">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="cfaa2-124">-Confirm</span></span>
<span data-ttu-id="cfaa2-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfaa2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfaa2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfaa2-126">-WhatIf</span></span>
<span data-ttu-id="cfaa2-127">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="cfaa2-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cfaa2-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cfaa2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfaa2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfaa2-129">CommonParameters</span></span>
<span data-ttu-id="cfaa2-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfaa2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfaa2-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cfaa2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfaa2-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="cfaa2-132">INPUTS</span></span>

### <span data-ttu-id="cfaa2-133">System.String</span><span class="sxs-lookup"><span data-stu-id="cfaa2-133">System.String</span></span>

### <span data-ttu-id="cfaa2-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="cfaa2-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="cfaa2-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="cfaa2-135">OUTPUTS</span></span>

### <span data-ttu-id="cfaa2-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cfaa2-136">System.Boolean</span></span>

## <span data-ttu-id="cfaa2-137">Notas</span><span class="sxs-lookup"><span data-stu-id="cfaa2-137">NOTES</span></span>

## <span data-ttu-id="cfaa2-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cfaa2-138">RELATED LINKS</span></span>
