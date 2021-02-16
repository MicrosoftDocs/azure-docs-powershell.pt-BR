---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelDataConnector.md
ms.openlocfilehash: e2505d53b0443bd048fb5d15df225adb0cba0980
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113999"
---
# <span data-ttu-id="24a01-101">Get-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="24a01-101">Get-AzSentinelDataConnector</span></span>

## <span data-ttu-id="24a01-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="24a01-102">SYNOPSIS</span></span>
<span data-ttu-id="24a01-103">Obter um Conector de Dados.</span><span class="sxs-lookup"><span data-stu-id="24a01-103">Get a Data Connector.</span></span>

## <span data-ttu-id="24a01-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="24a01-104">SYNTAX</span></span>

### <span data-ttu-id="24a01-105">WorkspaceScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="24a01-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24a01-106">DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="24a01-106">DataConnectorId</span></span>
```
Get-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24a01-107">Resourceid</span><span class="sxs-lookup"><span data-stu-id="24a01-107">ResourceId</span></span>
```
Get-AzSentinelDataConnector -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="24a01-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="24a01-108">DESCRIPTION</span></span>
<span data-ttu-id="24a01-109">O **cmdlet Get-AzSentinelDataConnector** obtém um Conector de Dados do espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="24a01-109">The **Get-AzSentinelDataConnector** cmdlet gets a Data Connector from the specified workspace.</span></span>
<span data-ttu-id="24a01-110">Se você especificar o parâmetro *DataConnectorId,* um único objeto **DataConnector** será retornado.</span><span class="sxs-lookup"><span data-stu-id="24a01-110">If you specify the *DataConnectorId* parameter, a single **DataConnector** object is returned.</span></span>
<span data-ttu-id="24a01-111">Se você não especificar o parâmetro *DataConnectorId,* uma matriz que contém todos os Conectores de Dados no espaço de trabalho especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="24a01-111">If you do not specify the *DataConnectorId* parameter, an array containing all of the Data Connectors in the specified workspace are returned.</span></span>
<span data-ttu-id="24a01-112">Você pode usar o **objeto DataConnector** para atualizar o Conector de Dados, por exemplo, você pode desabilitar o **DataConnector.**</span><span class="sxs-lookup"><span data-stu-id="24a01-112">You can use the **DataConnector** object to update the Data Connector, for example you can disable the **DataConnector**.</span></span>

## <span data-ttu-id="24a01-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="24a01-113">EXAMPLES</span></span>

### <span data-ttu-id="24a01-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="24a01-114">Example 1</span></span>
```powershell
PS C:\> $DataConnectors = Get-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="24a01-115">Este exemplo obtém todos os **DataConnectors** no espaço de trabalho especificado e o armazena na variável $DataConnectors dados.</span><span class="sxs-lookup"><span data-stu-id="24a01-115">This example gets all of the **DataConnectors** in the specified workspace, and then stores it in the $DataConnectors variable.</span></span>

### <span data-ttu-id="24a01-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="24a01-116">Example 2</span></span>
```powershell
PS C:\> $DataConnector = Get-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId"
```

<span data-ttu-id="24a01-117">Este exemplo obtém **um DataConnector** no espaço de trabalho especificado e o armazena na variável $DataConnector dados.</span><span class="sxs-lookup"><span data-stu-id="24a01-117">This example gets an **DataConnector** in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

## <span data-ttu-id="24a01-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24a01-118">PARAMETERS</span></span>

### <span data-ttu-id="24a01-119">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="24a01-119">-DataConnectorId</span></span>
<span data-ttu-id="24a01-120">ID do Conector de Dados.</span><span class="sxs-lookup"><span data-stu-id="24a01-120">Data Connector Id.</span></span>

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

### <span data-ttu-id="24a01-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24a01-121">-DefaultProfile</span></span>
<span data-ttu-id="24a01-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="24a01-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24a01-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24a01-123">-ResourceGroupName</span></span>
<span data-ttu-id="24a01-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="24a01-124">Resource group name.</span></span>

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

### <span data-ttu-id="24a01-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24a01-125">-ResourceId</span></span>
<span data-ttu-id="24a01-126">ID do Recurso.</span><span class="sxs-lookup"><span data-stu-id="24a01-126">Resource Id.</span></span>

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

### <span data-ttu-id="24a01-127">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="24a01-127">-WorkspaceName</span></span>
<span data-ttu-id="24a01-128">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="24a01-128">Workspace Name.</span></span>

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

### <span data-ttu-id="24a01-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24a01-129">CommonParameters</span></span>
<span data-ttu-id="24a01-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24a01-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24a01-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24a01-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24a01-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="24a01-132">INPUTS</span></span>

### <span data-ttu-id="24a01-133">System.String</span><span class="sxs-lookup"><span data-stu-id="24a01-133">System.String</span></span>
## <span data-ttu-id="24a01-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="24a01-134">OUTPUTS</span></span>

### <span data-ttu-id="24a01-135">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="24a01-135">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="24a01-136">Notas</span><span class="sxs-lookup"><span data-stu-id="24a01-136">NOTES</span></span>

## <span data-ttu-id="24a01-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="24a01-137">RELATED LINKS</span></span>
