---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelDataConnector.md
ms.openlocfilehash: 19e9dd843cd428a65b371ae933d00c58233de35b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117143"
---
# <span data-ttu-id="1b7be-101">Remove-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="1b7be-101">Remove-AzSentinelDataConnector</span></span>

## <span data-ttu-id="1b7be-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1b7be-102">SYNOPSIS</span></span>
<span data-ttu-id="1b7be-103">Remover um Conector de Dados.</span><span class="sxs-lookup"><span data-stu-id="1b7be-103">Remove a Data Connector.</span></span>

## <span data-ttu-id="1b7be-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1b7be-104">SYNTAX</span></span>

### <span data-ttu-id="1b7be-105">DataConnectorId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1b7be-105">DataConnectorId (Default)</span></span>
```
Remove-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b7be-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="1b7be-106">InputObject</span></span>
```
Remove-AzSentinelDataConnector -InputObject <PSSentinelDataConnector> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b7be-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="1b7be-107">DESCRIPTION</span></span>
<span data-ttu-id="1b7be-108">O cmdlet **Remove-AzSentinelDataConnector** exclui permanentemente um Conector de Dados de um espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="1b7be-108">The **Remove-AzSentinelDataConnector** cmdlet permanently deletes a Data Connector from a specified workspace.</span></span>
<span data-ttu-id="1b7be-109">Você pode passar um **objeto DataConnector** usando o operador de pipeline ou, alternativamente, pode especificar os parâmetros necessários.</span><span class="sxs-lookup"><span data-stu-id="1b7be-109">You can pass an **DataConnector** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="1b7be-110">Você pode usar o parâmetro Confirmar e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="1b7be-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="1b7be-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1b7be-111">EXAMPLES</span></span>

### <span data-ttu-id="1b7be-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1b7be-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId"
```

<span data-ttu-id="1b7be-113">Esse comando remove o DataConnector do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="1b7be-113">This command removes the DataConnector from the workspace.</span></span>

## <span data-ttu-id="1b7be-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1b7be-114">PARAMETERS</span></span>

### <span data-ttu-id="1b7be-115">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="1b7be-115">-DataConnectorId</span></span>
<span data-ttu-id="1b7be-116">ID do Conector de Dados.</span><span class="sxs-lookup"><span data-stu-id="1b7be-116">Data Connector Id.</span></span>

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

### <span data-ttu-id="1b7be-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b7be-117">-DefaultProfile</span></span>
<span data-ttu-id="1b7be-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1b7be-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b7be-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b7be-119">-InputObject</span></span>
<span data-ttu-id="1b7be-120">Inputobject.</span><span class="sxs-lookup"><span data-stu-id="1b7be-120">InputObject.</span></span>

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

### <span data-ttu-id="1b7be-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1b7be-121">-PassThru</span></span>
<span data-ttu-id="1b7be-122">Passthru</span><span class="sxs-lookup"><span data-stu-id="1b7be-122">PassThru</span></span>

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

### <span data-ttu-id="1b7be-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b7be-123">-ResourceGroupName</span></span>
<span data-ttu-id="1b7be-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1b7be-124">Resource group name.</span></span>

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

### <span data-ttu-id="1b7be-125">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="1b7be-125">-WorkspaceName</span></span>
<span data-ttu-id="1b7be-126">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="1b7be-126">Workspace Name.</span></span>

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

### <span data-ttu-id="1b7be-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="1b7be-127">-Confirm</span></span>
<span data-ttu-id="1b7be-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b7be-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b7be-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b7be-129">-WhatIf</span></span>
<span data-ttu-id="1b7be-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1b7be-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b7be-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1b7be-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b7be-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b7be-132">CommonParameters</span></span>
<span data-ttu-id="1b7be-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b7be-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b7be-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b7be-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b7be-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="1b7be-135">INPUTS</span></span>

### <span data-ttu-id="1b7be-136">System.String</span><span class="sxs-lookup"><span data-stu-id="1b7be-136">System.String</span></span>
### <span data-ttu-id="1b7be-137">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="1b7be-137">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="1b7be-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="1b7be-138">OUTPUTS</span></span>

### <span data-ttu-id="1b7be-139">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="1b7be-139">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="1b7be-140">Notas</span><span class="sxs-lookup"><span data-stu-id="1b7be-140">NOTES</span></span>

## <span data-ttu-id="1b7be-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1b7be-141">RELATED LINKS</span></span>
