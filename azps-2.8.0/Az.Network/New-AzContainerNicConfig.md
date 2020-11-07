---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-AzContainerNicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfig.md
ms.openlocfilehash: aaace7e8bb7d1f2ed57ebad28f7b5a3399f0e190
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772369"
---
# <span data-ttu-id="9fbe4-101">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="9fbe4-101">New-AzContainerNicConfig</span></span>

## <span data-ttu-id="9fbe4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9fbe4-102">SYNOPSIS</span></span>
<span data-ttu-id="9fbe4-103">Cria um novo objeto de configuração de interface de rede de contêiner.</span><span class="sxs-lookup"><span data-stu-id="9fbe4-103">Creates a new container network interface configuration object.</span></span>

## <span data-ttu-id="9fbe4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9fbe4-104">SYNTAX</span></span>

```
New-AzContainerNicConfig [-Name <String>] [-IpConfiguration <PSIPConfigurationProfile[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fbe4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9fbe4-105">DESCRIPTION</span></span>
<span data-ttu-id="9fbe4-106">O cmdlet **New-AzContainerNicConfig** cria um novo objeto de configuração de interface de rede de contêiner.</span><span class="sxs-lookup"><span data-stu-id="9fbe4-106">The **New-AzContainerNicConfig** cmdlet creates a new container network interface configuration object.</span></span> <span data-ttu-id="9fbe4-107">Esse objeto determina as características da interface de rede de contêiners criada para fazer referência ao perfil de rede pai.</span><span class="sxs-lookup"><span data-stu-id="9fbe4-107">This object determines the characteristics of container network interface created referencing the parent network profile.</span></span>

## <span data-ttu-id="9fbe4-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9fbe4-108">EXAMPLES</span></span>

### <span data-ttu-id="9fbe4-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9fbe4-109">Example 1</span></span>
```powershell
$containerNicConfig = New-AzContainerNicConfig -Name cnicConfig1

$networkProfile = New-AzNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="9fbe4-110">O primeiro comando cria uma configuração de interface de rede de contêiner vazia.</span><span class="sxs-lookup"><span data-stu-id="9fbe4-110">The first command creates an empty container network interface configuration.</span></span> <span data-ttu-id="9fbe4-111">O segundo cria um novo perfil de rede, passando a configuração da interface de rede de contêiner anteriormente criada como um argumento para o cmdlet New-NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="9fbe4-111">The second creates a new network profile, passing the previously created container network interface configuration as an argument to the New-NetworkProfile cmdlet.</span></span>

## <span data-ttu-id="9fbe4-112">OS</span><span class="sxs-lookup"><span data-stu-id="9fbe4-112">PARAMETERS</span></span>

### <span data-ttu-id="9fbe4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fbe4-113">-DefaultProfile</span></span>
<span data-ttu-id="9fbe4-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9fbe4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fbe4-115">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="9fbe4-115">-IpConfiguration</span></span>
<span data-ttu-id="9fbe4-116">Coleção de perfis de configuração de IP que determinam quais configurações de IP são criadas quando uma NIC de contêiner é instanciada nesta configuração de interface de rede de contêiner</span><span class="sxs-lookup"><span data-stu-id="9fbe4-116">Collection of IP configuration profiles which determine what ip configurations are created when a container nic is instantiated from this container network interface configuration</span></span>

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

### <span data-ttu-id="9fbe4-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="9fbe4-117">-Name</span></span>
<span data-ttu-id="9fbe4-118">Nome da configuração da interface de rede do contêiner.</span><span class="sxs-lookup"><span data-stu-id="9fbe4-118">Name of the container network interface configuration.</span></span>

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

### <span data-ttu-id="9fbe4-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9fbe4-119">-Confirm</span></span>
<span data-ttu-id="9fbe4-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fbe4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fbe4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fbe4-121">-WhatIf</span></span>
<span data-ttu-id="9fbe4-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9fbe4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fbe4-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9fbe4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fbe4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fbe4-124">CommonParameters</span></span>
<span data-ttu-id="9fbe4-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fbe4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fbe4-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fbe4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fbe4-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9fbe4-127">INPUTS</span></span>

### <span data-ttu-id="9fbe4-128">Microsoft. Azure. Commands. Network. Models. PSIPConfigurationProfile []</span><span class="sxs-lookup"><span data-stu-id="9fbe4-128">Microsoft.Azure.Commands.Network.Models.PSIPConfigurationProfile[]</span></span>

## <span data-ttu-id="9fbe4-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9fbe4-129">OUTPUTS</span></span>

### <span data-ttu-id="9fbe4-130">Microsoft. Azure. Commands. Network. Models. PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="9fbe4-130">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="9fbe4-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9fbe4-131">NOTES</span></span>

## <span data-ttu-id="9fbe4-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9fbe4-132">RELATED LINKS</span></span>

[<span data-ttu-id="9fbe4-133">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="9fbe4-133">New-AzContainerNicConfigIpConfig</span></span>](./New-AzContainerNicConfigIpConfig.md)