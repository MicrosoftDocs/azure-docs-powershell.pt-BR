---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelDataConnector.md
ms.openlocfilehash: 19e9dd843cd428a65b371ae933d00c58233de35b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433189"
---
# <span data-ttu-id="a7cd6-101">Remove-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="a7cd6-101">Remove-AzSentinelDataConnector</span></span>

## <span data-ttu-id="a7cd6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a7cd6-102">SYNOPSIS</span></span>
<span data-ttu-id="a7cd6-103">Remover um conector de dados.</span><span class="sxs-lookup"><span data-stu-id="a7cd6-103">Remove a Data Connector.</span></span>

## <span data-ttu-id="a7cd6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a7cd6-104">SYNTAX</span></span>

### <span data-ttu-id="a7cd6-105">Dataconnectorid (padrão)</span><span class="sxs-lookup"><span data-stu-id="a7cd6-105">DataConnectorId (Default)</span></span>
```
Remove-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7cd6-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a7cd6-106">InputObject</span></span>
```
Remove-AzSentinelDataConnector -InputObject <PSSentinelDataConnector> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7cd6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a7cd6-107">DESCRIPTION</span></span>
<span data-ttu-id="a7cd6-108">O cmdlet **Remove-AzSentinelDataConnector** exclui permanentemente um conector de dados de um espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="a7cd6-108">The **Remove-AzSentinelDataConnector** cmdlet permanently deletes a Data Connector from a specified workspace.</span></span>
<span data-ttu-id="a7cd6-109">Você pode passar um objeto **DataConnect** usando o operador pipeline ou, como alternativa, pode especificar os parâmetros obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="a7cd6-109">You can pass an **DataConnector** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="a7cd6-110">Você pode usar o parâmetro Confirm e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="a7cd6-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="a7cd6-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a7cd6-111">EXAMPLES</span></span>

### <span data-ttu-id="a7cd6-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a7cd6-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId"
```

<span data-ttu-id="a7cd6-113">Esse comando Remove o dataconnecter do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a7cd6-113">This command removes the DataConnector from the workspace.</span></span>

## <span data-ttu-id="a7cd6-114">OS</span><span class="sxs-lookup"><span data-stu-id="a7cd6-114">PARAMETERS</span></span>

### <span data-ttu-id="a7cd6-115">-Dataconnectorid</span><span class="sxs-lookup"><span data-stu-id="a7cd6-115">-DataConnectorId</span></span>
<span data-ttu-id="a7cd6-116">ID do conector de dados.</span><span class="sxs-lookup"><span data-stu-id="a7cd6-116">Data Connector Id.</span></span>

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

### <span data-ttu-id="a7cd6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7cd6-117">-DefaultProfile</span></span>
<span data-ttu-id="a7cd6-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a7cd6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7cd6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7cd6-119">-InputObject</span></span>
<span data-ttu-id="a7cd6-120">InputObject.</span><span class="sxs-lookup"><span data-stu-id="a7cd6-120">InputObject.</span></span>

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

### <span data-ttu-id="a7cd6-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a7cd6-121">-PassThru</span></span>
<span data-ttu-id="a7cd6-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="a7cd6-122">PassThru</span></span>

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

### <span data-ttu-id="a7cd6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7cd6-123">-ResourceGroupName</span></span>
<span data-ttu-id="a7cd6-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a7cd6-124">Resource group name.</span></span>

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

### <span data-ttu-id="a7cd6-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a7cd6-125">-WorkspaceName</span></span>
<span data-ttu-id="a7cd6-126">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a7cd6-126">Workspace Name.</span></span>

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

### <span data-ttu-id="a7cd6-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a7cd6-127">-Confirm</span></span>
<span data-ttu-id="a7cd6-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7cd6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7cd6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7cd6-129">-WhatIf</span></span>
<span data-ttu-id="a7cd6-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a7cd6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7cd6-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a7cd6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7cd6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7cd6-132">CommonParameters</span></span>
<span data-ttu-id="a7cd6-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7cd6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7cd6-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7cd6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7cd6-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a7cd6-135">INPUTS</span></span>

### <span data-ttu-id="a7cd6-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a7cd6-136">System.String</span></span>
### <span data-ttu-id="a7cd6-137">Microsoft. Azure. Commands. SecurityInsights. Models. dataconnecters. PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="a7cd6-137">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="a7cd6-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a7cd6-138">OUTPUTS</span></span>

### <span data-ttu-id="a7cd6-139">Microsoft. Azure. Commands. SecurityInsights. Models. dataconnecters. PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="a7cd6-139">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="a7cd6-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a7cd6-140">NOTES</span></span>

## <span data-ttu-id="a7cd6-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7cd6-141">RELATED LINKS</span></span>
