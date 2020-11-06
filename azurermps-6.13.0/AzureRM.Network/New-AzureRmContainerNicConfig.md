---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-AzureRmNetworkProfileContainerNicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmContainerNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmContainerNicConfig.md
ms.openlocfilehash: b697fcd991304401e2af754cc223f19b956f2143
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610872"
---
# <span data-ttu-id="14185-101">New-AzureRmNetworkProfileContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="14185-101">New-AzureRmNetworkProfileContainerNicConfig</span></span>

## <span data-ttu-id="14185-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="14185-102">SYNOPSIS</span></span>
<span data-ttu-id="14185-103">Cria um novo objeto de configuração de interface de rede de contêiner.</span><span class="sxs-lookup"><span data-stu-id="14185-103">Creates a new container network interface configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14185-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="14185-104">SYNTAX</span></span>

```
New-AzureRmNetworkProfileContainerNicConfig [-Name <String>] [-IpConfiguration <PSIPConfigurationProfile[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14185-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="14185-105">DESCRIPTION</span></span>
<span data-ttu-id="14185-106">O cmdlet **New-AzureRmNetworkProfileContainerNicConfig** cria um novo objeto de configuração de interface de rede de contêiner.</span><span class="sxs-lookup"><span data-stu-id="14185-106">The **New-AzureRmNetworkProfileContainerNicConfig** cmdlet creates a new container network interface configuration object.</span></span> <span data-ttu-id="14185-107">Esse objeto determina as características de interfacs de rede de contêiner criadas para fazer referência ao perfil de rede pai.</span><span class="sxs-lookup"><span data-stu-id="14185-107">This object determines the characteristics of container network interfacs created referencing the parent network profile.</span></span>

## <span data-ttu-id="14185-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="14185-108">EXAMPLES</span></span>

### <span data-ttu-id="14185-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="14185-109">Example 1</span></span>
```powershell
$containerNicConfig = New-AzureRmNetworkProfileContainerNicConfig -Name cnicConfig1

$networkProfile = New-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="14185-110">O primeiro comando cria uma configuração de interface de rede de contêiner vazia.</span><span class="sxs-lookup"><span data-stu-id="14185-110">The first command creates an empty container network interface configuration.</span></span> <span data-ttu-id="14185-111">O segundo cria um novo perfil de rede, passando a configuração da interface de rede de contêiner anteriormente criada como um argumento para o cmdlet New-NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="14185-111">The second creates a new network profile, passing the previously created container network interface configuration as an argument to the New-NetworkProfile cmdlet.</span></span>

## <span data-ttu-id="14185-112">OS</span><span class="sxs-lookup"><span data-stu-id="14185-112">PARAMETERS</span></span>

### <span data-ttu-id="14185-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14185-113">-DefaultProfile</span></span>
<span data-ttu-id="14185-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="14185-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14185-115">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="14185-115">-IpConfiguration</span></span>
<span data-ttu-id="14185-116">{{Preencher descrição da IpConfiguration}}</span><span class="sxs-lookup"><span data-stu-id="14185-116">{{Fill IpConfiguration Description}}</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIPConfigurationProfile[]
Parameter Sets: (All)
Aliases: IpConfig

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14185-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="14185-117">-Name</span></span>
<span data-ttu-id="14185-118">Nome da configuração da interface de rede do contêiner.</span><span class="sxs-lookup"><span data-stu-id="14185-118">Name of the container network interface configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14185-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="14185-119">-Confirm</span></span>
<span data-ttu-id="14185-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14185-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14185-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14185-121">-WhatIf</span></span>
<span data-ttu-id="14185-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="14185-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14185-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="14185-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14185-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14185-124">CommonParameters</span></span>
<span data-ttu-id="14185-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14185-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14185-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14185-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14185-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="14185-127">INPUTS</span></span>

### <span data-ttu-id="14185-128">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSIPConfigurationProfile, Microsoft. Azure. Commands. Network, Version = 6.7.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="14185-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSIPConfigurationProfile, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="14185-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="14185-129">OUTPUTS</span></span>

### <span data-ttu-id="14185-130">Microsoft. Azure. Commands. Network. Models. PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="14185-130">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="14185-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="14185-131">NOTES</span></span>

## <span data-ttu-id="14185-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14185-132">RELATED LINKS</span></span>
