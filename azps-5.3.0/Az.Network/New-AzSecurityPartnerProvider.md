---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
ms.openlocfilehash: 5af78bb1f915dec55f75749296340ca6d13a3b3d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433472"
---
# <span data-ttu-id="3791d-101">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3791d-101">New-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="3791d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3791d-102">SYNOPSIS</span></span>
<span data-ttu-id="3791d-103">Cria um SecurityPartnerProvider do Azure.</span><span class="sxs-lookup"><span data-stu-id="3791d-103">Creates an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="3791d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3791d-104">SYNTAX</span></span>

```
New-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> -Location <String>
 -SecurityProviderName <String> [-VirtualHub <PSVirtualHub>] [-VirtualHubId <String>]
 [-VirtualHubName <String>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3791d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3791d-105">DESCRIPTION</span></span>
<span data-ttu-id="3791d-106">O cmdlet **New-AzSecurityPartnerProvider** cria um Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3791d-106">The **New-AzSecurityPartnerProvider** cmdlet creates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="3791d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3791d-107">EXAMPLES</span></span>

### <span data-ttu-id="3791d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3791d-108">Example 1</span></span>
```powershell
 New-AzSecurityPartnerProvider -Name securityPartnerProviderName -ResourceGroupName rgname -Location 'West US' -SecurityProviderName 'ZScaler'
```

## <span data-ttu-id="3791d-109">OS</span><span class="sxs-lookup"><span data-stu-id="3791d-109">PARAMETERS</span></span>

### <span data-ttu-id="3791d-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3791d-110">-AsJob</span></span>
<span data-ttu-id="3791d-111">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3791d-111">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3791d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3791d-112">-DefaultProfile</span></span>
<span data-ttu-id="3791d-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3791d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3791d-114">-Force</span><span class="sxs-lookup"><span data-stu-id="3791d-114">-Force</span></span>
<span data-ttu-id="3791d-115">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="3791d-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3791d-116">-Local</span><span class="sxs-lookup"><span data-stu-id="3791d-116">-Location</span></span>
<span data-ttu-id="3791d-117">ponto.</span><span class="sxs-lookup"><span data-stu-id="3791d-117">location.</span></span>

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

### <span data-ttu-id="3791d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="3791d-118">-Name</span></span>
<span data-ttu-id="3791d-119">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="3791d-119">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3791d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3791d-120">-ResourceGroupName</span></span>
<span data-ttu-id="3791d-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3791d-121">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3791d-122">-SecurityProviderName</span><span class="sxs-lookup"><span data-stu-id="3791d-122">-SecurityProviderName</span></span>
<span data-ttu-id="3791d-123">O nome do provedor de segurança</span><span class="sxs-lookup"><span data-stu-id="3791d-123">The Security Provider name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ZScaler, IBoss, Checkpoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3791d-124">-Marca</span><span class="sxs-lookup"><span data-stu-id="3791d-124">-Tag</span></span>
<span data-ttu-id="3791d-125">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="3791d-125">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3791d-126">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="3791d-126">-VirtualHub</span></span>
<span data-ttu-id="3791d-127">A ID do Hub virtual à qual o provedor do parceiro de segurança está associado</span><span class="sxs-lookup"><span data-stu-id="3791d-127">The virtual hub Id that the security partner provider is attached to</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3791d-128">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="3791d-128">-VirtualHubId</span></span>
<span data-ttu-id="3791d-129">A ID do VirtualHub para o qual este VpnGateway precisa estar associado.</span><span class="sxs-lookup"><span data-stu-id="3791d-129">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="3791d-130">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="3791d-130">-VirtualHubName</span></span>
<span data-ttu-id="3791d-131">A ID do VirtualHub para o qual este VpnGateway precisa estar associado.</span><span class="sxs-lookup"><span data-stu-id="3791d-131">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="3791d-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3791d-132">-Confirm</span></span>
<span data-ttu-id="3791d-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3791d-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3791d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3791d-134">-WhatIf</span></span>
<span data-ttu-id="3791d-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3791d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3791d-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3791d-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3791d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3791d-137">CommonParameters</span></span>
<span data-ttu-id="3791d-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3791d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3791d-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3791d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3791d-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3791d-140">INPUTS</span></span>

### <span data-ttu-id="3791d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3791d-141">System.String</span></span>

### <span data-ttu-id="3791d-142">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="3791d-142">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="3791d-143">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3791d-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3791d-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3791d-144">OUTPUTS</span></span>

### <span data-ttu-id="3791d-145">Microsoft. Azure. Commands. Network. Models. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3791d-145">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="3791d-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3791d-146">NOTES</span></span>

## <span data-ttu-id="3791d-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3791d-147">RELATED LINKS</span></span>
