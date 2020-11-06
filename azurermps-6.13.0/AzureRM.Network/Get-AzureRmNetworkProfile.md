---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkProfile.md
ms.openlocfilehash: 5bdd5e5d5212564afb1f9b06f220e8c452bcbbaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441460"
---
# <span data-ttu-id="002bd-101">Get-AzureRmNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="002bd-101">Get-AzureRmNetworkProfile</span></span>

## <span data-ttu-id="002bd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="002bd-102">SYNOPSIS</span></span>
<span data-ttu-id="002bd-103">Obtém um recurso de nível superior do perfil de rede existente</span><span class="sxs-lookup"><span data-stu-id="002bd-103">Gets an existing network profile top level resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="002bd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="002bd-104">SYNTAX</span></span>

### <span data-ttu-id="002bd-105">NOEXPAND (padrão)</span><span class="sxs-lookup"><span data-stu-id="002bd-105">NoExpand (Default)</span></span>
```
Get-AzureRmNetworkProfile [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="002bd-106">GetByResourceNameExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="002bd-106">GetByResourceNameExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="002bd-107">GetByResourceNameNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="002bd-107">GetByResourceNameNoExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile [-ResourceGroupName <String>] [-Name <String>] -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="002bd-108">GetByResourceIdExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="002bd-108">GetByResourceIdExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile -ResourceId <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="002bd-109">GetByResourceIdNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="002bd-109">GetByResourceIdNoExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile -ResourceId <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="002bd-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="002bd-110">DESCRIPTION</span></span>
<span data-ttu-id="002bd-111">O cmdlet **Get-AzureRmNetworkProfile** recupera um recurso de nível superior de perfil de rede existente</span><span class="sxs-lookup"><span data-stu-id="002bd-111">The **Get-AzureRmNetworkProfile** cmdlet retrieves an existing network profile top level resource</span></span>

## <span data-ttu-id="002bd-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="002bd-112">EXAMPLES</span></span>

### <span data-ttu-id="002bd-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="002bd-113">Example 1</span></span>
```powershell
$networkProfile = Get-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="002bd-114">Isso recupera o perfil de rede NP1 na Rg1 de grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="002bd-114">This retrieves the network profile np1 in resource group rg1</span></span>

## <span data-ttu-id="002bd-115">OS</span><span class="sxs-lookup"><span data-stu-id="002bd-115">PARAMETERS</span></span>

### <span data-ttu-id="002bd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="002bd-116">-DefaultProfile</span></span>
<span data-ttu-id="002bd-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="002bd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="002bd-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="002bd-118">-ExpandResource</span></span>
<span data-ttu-id="002bd-119">A referência do recurso a ser expandida.</span><span class="sxs-lookup"><span data-stu-id="002bd-119">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet, GetByResourceNameNoExpandParameterSet, GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="002bd-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="002bd-120">-Name</span></span>
<span data-ttu-id="002bd-121">O nome do perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="002bd-121">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="002bd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="002bd-122">-ResourceGroupName</span></span>
<span data-ttu-id="002bd-123">O nome do grupo de recursos do perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="002bd-123">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="002bd-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="002bd-124">-ResourceId</span></span>
<span data-ttu-id="002bd-125">A ID do perfil de rede do Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="002bd-125">The Azure resource manager id of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="002bd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="002bd-126">CommonParameters</span></span>
<span data-ttu-id="002bd-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="002bd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="002bd-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="002bd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="002bd-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="002bd-129">INPUTS</span></span>

### <span data-ttu-id="002bd-130">System. String</span><span class="sxs-lookup"><span data-stu-id="002bd-130">System.String</span></span>

## <span data-ttu-id="002bd-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="002bd-131">OUTPUTS</span></span>

### <span data-ttu-id="002bd-132">Microsoft. Azure. Commands. Network. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="002bd-132">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="002bd-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="002bd-133">NOTES</span></span>

## <span data-ttu-id="002bd-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="002bd-134">RELATED LINKS</span></span>
