---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/remove-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelDataConnector.md
ms.openlocfilehash: d9dc64124dd4840227b692e2ef21842a19b4adeb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888652"
---
# <span data-ttu-id="688dc-101">Remove-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="688dc-101">Remove-AzSentinelDataConnector</span></span>

## <span data-ttu-id="688dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="688dc-102">SYNOPSIS</span></span>
<span data-ttu-id="688dc-103">Remover um Conector de Dados.</span><span class="sxs-lookup"><span data-stu-id="688dc-103">Remove a Data Connector.</span></span>

## <span data-ttu-id="688dc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="688dc-104">SYNTAX</span></span>

### <span data-ttu-id="688dc-105">DataConnectorId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="688dc-105">DataConnectorId (Default)</span></span>
```
Remove-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="688dc-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="688dc-106">InputObject</span></span>
```
Remove-AzSentinelDataConnector -InputObject <PSSentinelDataConnector> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="688dc-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="688dc-107">DESCRIPTION</span></span>
<span data-ttu-id="688dc-108">O cmdlet **Remove-AzSentinelDataConnector** exclui permanentemente um Conector de Dados de um espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="688dc-108">The **Remove-AzSentinelDataConnector** cmdlet permanently deletes a Data Connector from a specified workspace.</span></span>
<span data-ttu-id="688dc-109">Você pode passar **um objeto DataConnector** usando o operador de pipeline ou, como alternativa, pode especificar os parâmetros necessários.</span><span class="sxs-lookup"><span data-stu-id="688dc-109">You can pass an **DataConnector** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="688dc-110">Você pode usar o parâmetro Confirm e $ConfirmPreference Windows PowerShell para controlar se o cmdlet solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="688dc-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="688dc-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="688dc-111">EXAMPLES</span></span>

### <span data-ttu-id="688dc-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="688dc-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId"
```

<span data-ttu-id="688dc-113">Este comando remove o DataConnector do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="688dc-113">This command removes the DataConnector from the workspace.</span></span>

## <span data-ttu-id="688dc-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="688dc-114">PARAMETERS</span></span>

### <span data-ttu-id="688dc-115">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="688dc-115">-DataConnectorId</span></span>
<span data-ttu-id="688dc-116">ID do Conector de Dados.</span><span class="sxs-lookup"><span data-stu-id="688dc-116">Data Connector Id.</span></span>

```yaml
Type: System.String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="688dc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="688dc-117">-DefaultProfile</span></span>
<span data-ttu-id="688dc-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="688dc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="688dc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="688dc-119">-InputObject</span></span>
<span data-ttu-id="688dc-120">InputObject.</span><span class="sxs-lookup"><span data-stu-id="688dc-120">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="688dc-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="688dc-121">-PassThru</span></span>
<span data-ttu-id="688dc-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="688dc-122">PassThru</span></span>

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

### <span data-ttu-id="688dc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="688dc-123">-ResourceGroupName</span></span>
<span data-ttu-id="688dc-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="688dc-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="688dc-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="688dc-125">-WorkspaceName</span></span>
<span data-ttu-id="688dc-126">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="688dc-126">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="688dc-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="688dc-127">-Confirm</span></span>
<span data-ttu-id="688dc-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="688dc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="688dc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="688dc-129">-WhatIf</span></span>
<span data-ttu-id="688dc-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="688dc-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="688dc-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="688dc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="688dc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="688dc-132">CommonParameters</span></span>
<span data-ttu-id="688dc-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="688dc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="688dc-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="688dc-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="688dc-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="688dc-135">INPUTS</span></span>

### <span data-ttu-id="688dc-136">System.String</span><span class="sxs-lookup"><span data-stu-id="688dc-136">System.String</span></span>
### <span data-ttu-id="688dc-137">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="688dc-137">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="688dc-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="688dc-138">OUTPUTS</span></span>

### <span data-ttu-id="688dc-139">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="688dc-139">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="688dc-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="688dc-140">NOTES</span></span>

## <span data-ttu-id="688dc-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="688dc-141">RELATED LINKS</span></span>
