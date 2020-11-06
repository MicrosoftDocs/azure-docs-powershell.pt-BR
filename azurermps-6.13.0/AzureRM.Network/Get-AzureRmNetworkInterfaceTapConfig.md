---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceTapConfig.md
ms.openlocfilehash: 2f6c4f410c7d4f92c8dcd911e0c113f2a91b304c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611035"
---
# <span data-ttu-id="c0550-101">Get-AzureRmNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="c0550-101">Get-AzureRmNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="c0550-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c0550-102">SYNOPSIS</span></span>
<span data-ttu-id="c0550-103">Obtém um recurso de configuração do toque.</span><span class="sxs-lookup"><span data-stu-id="c0550-103">Gets a Tap configuration resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0550-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c0550-104">SYNTAX</span></span>

### <span data-ttu-id="c0550-105">GetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c0550-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzureRmNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0550-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0550-106">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmNetworkInterfaceTapConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0550-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c0550-107">DESCRIPTION</span></span>
<span data-ttu-id="c0550-108">O cmdlet **Get-AzureRmNetworkInterfaceTapConfig** Obtém uma configuração do Azure TAP para um determinado grupo de recursos, interface de rede e toque em nome de configuração ou lista de configurações de toque em um grupo de recursos e em uma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="c0550-108">The **Get-AzureRmNetworkInterfaceTapConfig** cmdlet gets an Azure Tap Configuration for a given resource group, network interface and tap configuration name or list of tap configurations in a resource group and network interface.</span></span>

## <span data-ttu-id="c0550-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c0550-109">EXAMPLES</span></span>

### <span data-ttu-id="c0550-110">Exemplo 1: obter todas as configurações de toque para uma determinada interface de rede</span><span class="sxs-lookup"><span data-stu-id="c0550-110">Example 1: Get all tap configurations for a given network interface</span></span>
```
PS C:\>Get-AzureRmNetworkInterfaceTapConfig -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName"
```

<span data-ttu-id="c0550-111">Esse comando obtém configurações de toque adicionadas para a interface de rede fornecida.</span><span class="sxs-lookup"><span data-stu-id="c0550-111">This command gets tap configurations added for the given network interface.</span></span>

### <span data-ttu-id="c0550-112">Exemplo 2: obter uma determinada configuração de toque</span><span class="sxs-lookup"><span data-stu-id="c0550-112">Example 2: Get a given tap configuration</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
```

<span data-ttu-id="c0550-113">Esse comando obtém uma configuração de toque específico adicionada para a interface de rede fornecida.</span><span class="sxs-lookup"><span data-stu-id="c0550-113">This command gets specific tap configuration added for the given network interface.</span></span>

## <span data-ttu-id="c0550-114">OS</span><span class="sxs-lookup"><span data-stu-id="c0550-114">PARAMETERS</span></span>

### <span data-ttu-id="c0550-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0550-115">-DefaultProfile</span></span>
<span data-ttu-id="c0550-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c0550-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0550-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="c0550-117">-Name</span></span>
<span data-ttu-id="c0550-118">Nome da configuração do toque específico.</span><span class="sxs-lookup"><span data-stu-id="c0550-118">Name of the specific tap configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0550-119">-NetworkInterfacename</span><span class="sxs-lookup"><span data-stu-id="c0550-119">-NetworkInterfaceName</span></span>
<span data-ttu-id="c0550-120">O nome da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="c0550-120">The Network Interface name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0550-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0550-121">-ResourceGroupName</span></span>
<span data-ttu-id="c0550-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c0550-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0550-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0550-123">-ResourceId</span></span>
<span data-ttu-id="c0550-124">ResourceId do recurso TapConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0550-124">ResourceId of the TapConfiguration resource</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0550-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c0550-125">-Confirm</span></span>
<span data-ttu-id="c0550-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0550-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0550-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0550-127">-WhatIf</span></span>
<span data-ttu-id="c0550-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c0550-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c0550-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c0550-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0550-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0550-130">CommonParameters</span></span>
<span data-ttu-id="c0550-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0550-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0550-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0550-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0550-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c0550-133">INPUTS</span></span>

### <span data-ttu-id="c0550-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c0550-134">System.String</span></span>

## <span data-ttu-id="c0550-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c0550-135">OUTPUTS</span></span>

### <span data-ttu-id="c0550-136">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0550-136">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="c0550-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c0550-137">NOTES</span></span>

## <span data-ttu-id="c0550-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c0550-138">RELATED LINKS</span></span>
