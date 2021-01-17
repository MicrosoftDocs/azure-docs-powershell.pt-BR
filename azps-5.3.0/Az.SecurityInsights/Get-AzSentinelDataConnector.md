---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelDataConnector.md
ms.openlocfilehash: e2505d53b0443bd048fb5d15df225adb0cba0980
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433214"
---
# <span data-ttu-id="ed187-101">Get-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="ed187-101">Get-AzSentinelDataConnector</span></span>

## <span data-ttu-id="ed187-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ed187-102">SYNOPSIS</span></span>
<span data-ttu-id="ed187-103">Obter um conector de dados.</span><span class="sxs-lookup"><span data-stu-id="ed187-103">Get a Data Connector.</span></span>

## <span data-ttu-id="ed187-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed187-104">SYNTAX</span></span>

### <span data-ttu-id="ed187-105">WorkspaceScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="ed187-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed187-106">Dataconnectorid</span><span class="sxs-lookup"><span data-stu-id="ed187-106">DataConnectorId</span></span>
```
Get-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed187-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="ed187-107">ResourceId</span></span>
```
Get-AzSentinelDataConnector -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed187-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ed187-108">DESCRIPTION</span></span>
<span data-ttu-id="ed187-109">O cmdlet **Get-AzSentinelDataConnector** Obtém um conector de dados do espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="ed187-109">The **Get-AzSentinelDataConnector** cmdlet gets a Data Connector from the specified workspace.</span></span>
<span data-ttu-id="ed187-110">Se você especificar o parâmetro *Dataconnectorid* , um único objeto **dataconnecter** será retornado.</span><span class="sxs-lookup"><span data-stu-id="ed187-110">If you specify the *DataConnectorId* parameter, a single **DataConnector** object is returned.</span></span>
<span data-ttu-id="ed187-111">Se você não especificar o parâmetro *Dataconnectorid* , uma matriz contendo todos os conectores de dados no espaço de trabalho especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="ed187-111">If you do not specify the *DataConnectorId* parameter, an array containing all of the Data Connectors in the specified workspace are returned.</span></span>
<span data-ttu-id="ed187-112">Você pode usar o objeto **Dataconnecter** para atualizar o conector de dados, por exemplo, você pode desabilitar o **dataconnecter**.</span><span class="sxs-lookup"><span data-stu-id="ed187-112">You can use the **DataConnector** object to update the Data Connector, for example you can disable the **DataConnector**.</span></span>

## <span data-ttu-id="ed187-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ed187-113">EXAMPLES</span></span>

### <span data-ttu-id="ed187-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ed187-114">Example 1</span></span>
```powershell
PS C:\> $DataConnectors = Get-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="ed187-115">Este exemplo obtém todos os **Dataconnecters** do espaço de trabalho especificado e, em seguida, armazena-os na variável $DataConnectors.</span><span class="sxs-lookup"><span data-stu-id="ed187-115">This example gets all of the **DataConnectors** in the specified workspace, and then stores it in the $DataConnectors variable.</span></span>

### <span data-ttu-id="ed187-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ed187-116">Example 2</span></span>
```powershell
PS C:\> $DataConnector = Get-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId"
```

<span data-ttu-id="ed187-117">Este exemplo obtém um **Dataconnecter** no espaço de trabalho especificado e, em seguida, armazena-o na variável $DataConnector.</span><span class="sxs-lookup"><span data-stu-id="ed187-117">This example gets an **DataConnector** in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

## <span data-ttu-id="ed187-118">OS</span><span class="sxs-lookup"><span data-stu-id="ed187-118">PARAMETERS</span></span>

### <span data-ttu-id="ed187-119">-Dataconnectorid</span><span class="sxs-lookup"><span data-stu-id="ed187-119">-DataConnectorId</span></span>
<span data-ttu-id="ed187-120">ID do conector de dados.</span><span class="sxs-lookup"><span data-stu-id="ed187-120">Data Connector Id.</span></span>

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

### <span data-ttu-id="ed187-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed187-121">-DefaultProfile</span></span>
<span data-ttu-id="ed187-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ed187-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed187-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed187-123">-ResourceGroupName</span></span>
<span data-ttu-id="ed187-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ed187-124">Resource group name.</span></span>

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

### <span data-ttu-id="ed187-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed187-125">-ResourceId</span></span>
<span data-ttu-id="ed187-126">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="ed187-126">Resource Id.</span></span>

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

### <span data-ttu-id="ed187-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ed187-127">-WorkspaceName</span></span>
<span data-ttu-id="ed187-128">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ed187-128">Workspace Name.</span></span>

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

### <span data-ttu-id="ed187-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed187-129">CommonParameters</span></span>
<span data-ttu-id="ed187-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed187-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed187-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed187-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed187-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ed187-132">INPUTS</span></span>

### <span data-ttu-id="ed187-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ed187-133">System.String</span></span>
## <span data-ttu-id="ed187-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ed187-134">OUTPUTS</span></span>

### <span data-ttu-id="ed187-135">Microsoft. Azure. Commands. SecurityInsights. Models. dataconnecters. PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="ed187-135">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="ed187-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ed187-136">NOTES</span></span>

## <span data-ttu-id="ed187-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed187-137">RELATED LINKS</span></span>
