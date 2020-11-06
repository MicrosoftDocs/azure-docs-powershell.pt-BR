---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkProfile.md
ms.openlocfilehash: 87d753ebaf2d8d4891fc96dbc25f7ad0fa1095af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600307"
---
# <span data-ttu-id="9ed87-101">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9ed87-101">New-AzNetworkProfile</span></span>

## <span data-ttu-id="9ed87-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9ed87-102">SYNOPSIS</span></span>
<span data-ttu-id="9ed87-103">Cria um novo perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="9ed87-103">Creates a new network profile.</span></span>

## <span data-ttu-id="9ed87-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ed87-104">SYNTAX</span></span>

```
New-AzNetworkProfile -ResourceGroupName <String> -Name <String> [-Location <String>] [-Tag <Hashtable>]
 [-ContainerNicConfig <PSContainerNetworkInterfaceConfiguration[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ed87-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9ed87-105">DESCRIPTION</span></span>
<span data-ttu-id="9ed87-106">O cmdlet **New-AzNetworkProfile** cria um novo recurso de nível superior do perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="9ed87-106">The **New-AzNetworkProfile** cmdlet creates a new network profile top level resource.</span></span>

## <span data-ttu-id="9ed87-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9ed87-107">EXAMPLES</span></span>

### <span data-ttu-id="9ed87-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9ed87-108">Example 1</span></span>
```powershell
$networkProfile = New-AzNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus
```

<span data-ttu-id="9ed87-109">Isso cria um novo recurso de nível superior do perfil de rede</span><span class="sxs-lookup"><span data-stu-id="9ed87-109">This creates a new network profile top level resource</span></span>

## <span data-ttu-id="9ed87-110">OS</span><span class="sxs-lookup"><span data-stu-id="9ed87-110">PARAMETERS</span></span>

### <span data-ttu-id="9ed87-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ed87-111">-AsJob</span></span>
<span data-ttu-id="9ed87-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9ed87-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9ed87-113">-ContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="9ed87-113">-ContainerNicConfig</span></span>
<span data-ttu-id="9ed87-114">As configurações de interface de rede de contêiner para adicionar a este perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="9ed87-114">The container network interface configurations to add to this network profile.</span></span>

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

### <span data-ttu-id="9ed87-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ed87-115">-DefaultProfile</span></span>
<span data-ttu-id="9ed87-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9ed87-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ed87-117">-Force</span><span class="sxs-lookup"><span data-stu-id="9ed87-117">-Force</span></span>
<span data-ttu-id="9ed87-118">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="9ed87-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="9ed87-119">-Local</span><span class="sxs-lookup"><span data-stu-id="9ed87-119">-Location</span></span>
<span data-ttu-id="9ed87-120">O local.</span><span class="sxs-lookup"><span data-stu-id="9ed87-120">The location.</span></span>

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

### <span data-ttu-id="9ed87-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="9ed87-121">-Name</span></span>
<span data-ttu-id="9ed87-122">O nome do perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="9ed87-122">The name of the network profile.</span></span>

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

### <span data-ttu-id="9ed87-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ed87-123">-ResourceGroupName</span></span>
<span data-ttu-id="9ed87-124">O nome do grupo de recursos do perfil de rede.</span><span class="sxs-lookup"><span data-stu-id="9ed87-124">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="9ed87-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="9ed87-125">-Tag</span></span>
<span data-ttu-id="9ed87-126">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="9ed87-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="9ed87-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9ed87-127">-Confirm</span></span>
<span data-ttu-id="9ed87-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ed87-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ed87-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ed87-129">-WhatIf</span></span>
<span data-ttu-id="9ed87-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9ed87-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ed87-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9ed87-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ed87-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ed87-132">CommonParameters</span></span>
<span data-ttu-id="9ed87-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ed87-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ed87-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ed87-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ed87-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9ed87-135">INPUTS</span></span>

### <span data-ttu-id="9ed87-136">System. String</span><span class="sxs-lookup"><span data-stu-id="9ed87-136">System.String</span></span>

### <span data-ttu-id="9ed87-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9ed87-137">System.Collections.Hashtable</span></span>

### <span data-ttu-id="9ed87-138">Microsoft. Azure. Commands. Network. Models. PSContainerNetworkInterfaceConfiguration []</span><span class="sxs-lookup"><span data-stu-id="9ed87-138">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration[]</span></span>

## <span data-ttu-id="9ed87-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9ed87-139">OUTPUTS</span></span>

### <span data-ttu-id="9ed87-140">Microsoft. Azure. Commands. Network. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9ed87-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="9ed87-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9ed87-141">NOTES</span></span>

## <span data-ttu-id="9ed87-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9ed87-142">RELATED LINKS</span></span>

[<span data-ttu-id="9ed87-143">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9ed87-143">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="9ed87-144">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9ed87-144">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)

[<span data-ttu-id="9ed87-145">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9ed87-145">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
