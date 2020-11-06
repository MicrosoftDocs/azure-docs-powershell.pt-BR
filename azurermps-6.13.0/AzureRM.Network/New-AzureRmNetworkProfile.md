---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkProfile.md
ms.openlocfilehash: fedf6818f95bd5afadb92c1423a1dbb3296727e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430144"
---
# <span data-ttu-id="fbb9b-101">New-AzureRmNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="fbb9b-101">New-AzureRmNetworkProfile</span></span>

## <span data-ttu-id="fbb9b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fbb9b-102">SYNOPSIS</span></span>
<span data-ttu-id="fbb9b-103">Cria um novo perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="fbb9b-103">Creates a new network profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbb9b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fbb9b-104">SYNTAX</span></span>

```
New-AzureRmNetworkProfile -ResourceGroupName <String> -Name <String> [-Location <String>] [-Tag <Hashtable>]
 [-ContainerNicConfig <PSContainerNetworkInterfaceConfiguration[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbb9b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fbb9b-105">DESCRIPTION</span></span>
<span data-ttu-id="fbb9b-106">O cmdlet **New-AzureRmNetworkProfile** cria um novo recurso de nível superior do perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="fbb9b-106">The **New-AzureRmNetworkProfile** cmdlet creates a new network profile top level resource.</span></span>

## <span data-ttu-id="fbb9b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fbb9b-107">EXAMPLES</span></span>

### <span data-ttu-id="fbb9b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fbb9b-108">Example 1</span></span>
```powershell
$networkProfile = New-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus
```

<span data-ttu-id="fbb9b-109">Isso cria um novo recurso de nível superior do perfil de rede</span><span class="sxs-lookup"><span data-stu-id="fbb9b-109">This creates a new network profile top level resource</span></span>

## <span data-ttu-id="fbb9b-110">OS</span><span class="sxs-lookup"><span data-stu-id="fbb9b-110">PARAMETERS</span></span>

### <span data-ttu-id="fbb9b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fbb9b-111">-AsJob</span></span>
<span data-ttu-id="fbb9b-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="fbb9b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fbb9b-113">-ContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="fbb9b-113">-ContainerNicConfig</span></span>
<span data-ttu-id="fbb9b-114">As configurações de interface de rede de contêiner para adicionar a este perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="fbb9b-114">The container network interface configurations to add to this network profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration[]
Parameter Sets: (All)
Aliases: ContainerNetworkInterfaceConfiguration

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbb9b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbb9b-115">-DefaultProfile</span></span>
<span data-ttu-id="fbb9b-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fbb9b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbb9b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="fbb9b-117">-Force</span></span>
<span data-ttu-id="fbb9b-118">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="fbb9b-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="fbb9b-119">-Local</span><span class="sxs-lookup"><span data-stu-id="fbb9b-119">-Location</span></span>
<span data-ttu-id="fbb9b-120">O local.</span><span class="sxs-lookup"><span data-stu-id="fbb9b-120">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbb9b-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="fbb9b-121">-Name</span></span>
<span data-ttu-id="fbb9b-122">O nome do perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="fbb9b-122">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbb9b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbb9b-123">-ResourceGroupName</span></span>
<span data-ttu-id="fbb9b-124">O nome do grupo de recursos do perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="fbb9b-124">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbb9b-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="fbb9b-125">-Tag</span></span>
<span data-ttu-id="fbb9b-126">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="fbb9b-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbb9b-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fbb9b-127">-Confirm</span></span>
<span data-ttu-id="fbb9b-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbb9b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbb9b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbb9b-129">-WhatIf</span></span>
<span data-ttu-id="fbb9b-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fbb9b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbb9b-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fbb9b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbb9b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbb9b-132">CommonParameters</span></span>
<span data-ttu-id="fbb9b-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbb9b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbb9b-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbb9b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbb9b-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fbb9b-135">INPUTS</span></span>

### <span data-ttu-id="fbb9b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="fbb9b-136">System.String</span></span>

### <span data-ttu-id="fbb9b-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fbb9b-137">System.Collections.Hashtable</span></span>

### <span data-ttu-id="fbb9b-138">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSContainerNetworkInterface, Microsoft. Azure. Commands. Network, Version = 6.7.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="fbb9b-138">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterface, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="fbb9b-139">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSContainerNetworkInterfaceConfiguration, Microsoft. Azure. Commands. Network, Version = 6.7.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="fbb9b-139">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="fbb9b-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fbb9b-140">OUTPUTS</span></span>

### <span data-ttu-id="fbb9b-141">Microsoft. Azure. Commands. Network. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="fbb9b-141">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="fbb9b-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fbb9b-142">NOTES</span></span>

## <span data-ttu-id="fbb9b-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fbb9b-143">RELATED LINKS</span></span>
