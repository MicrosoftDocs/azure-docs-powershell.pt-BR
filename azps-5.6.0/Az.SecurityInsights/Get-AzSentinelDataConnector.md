---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/get-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelDataConnector.md
ms.openlocfilehash: b99ad26ddfa0239f073c4179413b2f1fefec4d1b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889729"
---
# <span data-ttu-id="63ee3-101">Get-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="63ee3-101">Get-AzSentinelDataConnector</span></span>

## <span data-ttu-id="63ee3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63ee3-102">SYNOPSIS</span></span>
<span data-ttu-id="63ee3-103">Obter um Conector de Dados.</span><span class="sxs-lookup"><span data-stu-id="63ee3-103">Get a Data Connector.</span></span>

## <span data-ttu-id="63ee3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="63ee3-104">SYNTAX</span></span>

### <span data-ttu-id="63ee3-105">WorkspaceScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="63ee3-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63ee3-106">DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="63ee3-106">DataConnectorId</span></span>
```
Get-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63ee3-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="63ee3-107">ResourceId</span></span>
```
Get-AzSentinelDataConnector -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="63ee3-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="63ee3-108">DESCRIPTION</span></span>
<span data-ttu-id="63ee3-109">O cmdlet **Get-AzSentinelDataConnector** obtém um Conector de Dados do espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="63ee3-109">The **Get-AzSentinelDataConnector** cmdlet gets a Data Connector from the specified workspace.</span></span>
<span data-ttu-id="63ee3-110">Se você especificar o *parâmetro DataConnectorId,* um único **objeto DataConnector** será retornado.</span><span class="sxs-lookup"><span data-stu-id="63ee3-110">If you specify the *DataConnectorId* parameter, a single **DataConnector** object is returned.</span></span>
<span data-ttu-id="63ee3-111">Se você não especificar o parâmetro *DataConnectorId,* uma matriz contendo todos os Conectores de Dados no espaço de trabalho especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="63ee3-111">If you do not specify the *DataConnectorId* parameter, an array containing all of the Data Connectors in the specified workspace are returned.</span></span>
<span data-ttu-id="63ee3-112">Você pode usar o **objeto DataConnector** para atualizar o Conector de Dados, por exemplo, você pode desabilitar **o DataConnector**.</span><span class="sxs-lookup"><span data-stu-id="63ee3-112">You can use the **DataConnector** object to update the Data Connector, for example you can disable the **DataConnector**.</span></span>

## <span data-ttu-id="63ee3-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="63ee3-113">EXAMPLES</span></span>

### <span data-ttu-id="63ee3-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="63ee3-114">Example 1</span></span>
```powershell
PS C:\> $DataConnectors = Get-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="63ee3-115">Este exemplo obtém todos os **DataConnectors** no espaço de trabalho especificado e o armazena na variável $DataConnectors.</span><span class="sxs-lookup"><span data-stu-id="63ee3-115">This example gets all of the **DataConnectors** in the specified workspace, and then stores it in the $DataConnectors variable.</span></span>

### <span data-ttu-id="63ee3-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="63ee3-116">Example 2</span></span>
```powershell
PS C:\> $DataConnector = Get-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId"
```

<span data-ttu-id="63ee3-117">Este exemplo obtém **um DataConnector** no espaço de trabalho especificado e o armazena na variável $DataConnector.</span><span class="sxs-lookup"><span data-stu-id="63ee3-117">This example gets an **DataConnector** in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

## <span data-ttu-id="63ee3-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="63ee3-118">PARAMETERS</span></span>

### <span data-ttu-id="63ee3-119">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="63ee3-119">-DataConnectorId</span></span>
<span data-ttu-id="63ee3-120">ID do Conector de Dados.</span><span class="sxs-lookup"><span data-stu-id="63ee3-120">Data Connector Id.</span></span>

```yaml
Type: System.String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63ee3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63ee3-121">-DefaultProfile</span></span>
<span data-ttu-id="63ee3-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="63ee3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63ee3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63ee3-123">-ResourceGroupName</span></span>
<span data-ttu-id="63ee3-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="63ee3-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63ee3-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63ee3-125">-ResourceId</span></span>
<span data-ttu-id="63ee3-126">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="63ee3-126">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63ee3-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="63ee3-127">-WorkspaceName</span></span>
<span data-ttu-id="63ee3-128">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="63ee3-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63ee3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63ee3-129">CommonParameters</span></span>
<span data-ttu-id="63ee3-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63ee3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63ee3-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63ee3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63ee3-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="63ee3-132">INPUTS</span></span>

### <span data-ttu-id="63ee3-133">System.String</span><span class="sxs-lookup"><span data-stu-id="63ee3-133">System.String</span></span>
## <span data-ttu-id="63ee3-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="63ee3-134">OUTPUTS</span></span>

### <span data-ttu-id="63ee3-135">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="63ee3-135">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="63ee3-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="63ee3-136">NOTES</span></span>

## <span data-ttu-id="63ee3-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="63ee3-137">RELATED LINKS</span></span>
