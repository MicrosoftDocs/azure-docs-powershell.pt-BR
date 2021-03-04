---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azappserviceenvironmentinboundservices
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServiceEnvironmentInboundServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServiceEnvironmentInboundServices.md
ms.openlocfilehash: 68b2957e959365187ad82980bd2be2f055632a57
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891916"
---
# <span data-ttu-id="e5d6f-101">New-AzAppServiceEnvironmentInboundServices</span><span class="sxs-lookup"><span data-stu-id="e5d6f-101">New-AzAppServiceEnvironmentInboundServices</span></span>

## <span data-ttu-id="e5d6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5d6f-102">SYNOPSIS</span></span>
<span data-ttu-id="e5d6f-103">Cria serviços de entrada para o Ambiente de Serviço de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e5d6f-103">Creates inbound services for App Service Environment.</span></span> <span data-ttu-id="e5d6f-104">Para iLB ASEv2, isso criará uma Zona DNS Privada do Azure e registros para mapear para o IP interno.</span><span class="sxs-lookup"><span data-stu-id="e5d6f-104">For ASEv2 ILB, this will create an Azure Private DNS Zone and records to map to the internal IP.</span></span> <span data-ttu-id="e5d6f-105">Para ASEv3, ele também garantirá que a sub-rede tenha a Política de Rede desabilitada e criará um ponto de extremidade privado.</span><span class="sxs-lookup"><span data-stu-id="e5d6f-105">For ASEv3 it will in addition ensure subnet has Network Policy disabled and will create a private endpoint.</span></span>

## <span data-ttu-id="e5d6f-106">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e5d6f-106">SYNTAX</span></span>

### <span data-ttu-id="e5d6f-107">SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5d6f-107">SubnetNameParameterSet</span></span>
```
New-AzAppServiceEnvironmentInboundServices [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkName <String> -SubnetName <String> [-SkipDns] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5d6f-108">SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5d6f-108">SubnetIdParameterSet</span></span>
```
New-AzAppServiceEnvironmentInboundServices [-ResourceGroupName] <String> [-Name] <String> -SubnetId <String>
 [-SkipDns] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5d6f-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e5d6f-109">DESCRIPTION</span></span>
<span data-ttu-id="e5d6f-110">O cmdlet **New-AzAppServiceEnvironmentInboundServices** cria serviços de entrada para um ambiente de serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e5d6f-110">The **New-AzAppServiceEnvironmentInboundServices** cmdlet create inbound services for an App Service Environment.</span></span>

## <span data-ttu-id="e5d6f-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e5d6f-111">EXAMPLES</span></span>

### <span data-ttu-id="e5d6f-112">Exemplo 1: Criar zona DNS privada e registros para ASEv2</span><span class="sxs-lookup"><span data-stu-id="e5d6f-112">Example 1: Create Private DNS Zone and records for ASEv2</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironmentInboundServices -ResourceGroupName AseResourceGroup -Name AseV2Name
-VirtualNetworkName MyVirtualNetwork -SubnetName InboundSubnet
```

<span data-ttu-id="e5d6f-113">Criar zona DNS privada e registros para ASEv2</span><span class="sxs-lookup"><span data-stu-id="e5d6f-113">Create Private DNS Zone and records for ASEv2</span></span>

### <span data-ttu-id="e5d6f-114">Exemplo 2: Criar ponto de extremidade privado, Zona DNS Privada e registros para ASEv3</span><span class="sxs-lookup"><span data-stu-id="e5d6f-114">Example 2: Create private endpoint, Private DNS Zone and records for ASEv3</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironmentInboundServices -ResourceGroupName AseResourceGroup -Name AseV2Name
-VirtualNetworkName MyVirtualNetwork -SubnetName InboundSubnet
```

<span data-ttu-id="e5d6f-115">Criar ponto de extremidade privado, Zona DNS Privada e registros para ASEv3</span><span class="sxs-lookup"><span data-stu-id="e5d6f-115">Create private endpoint, Private DNS Zone and records for ASEv3</span></span>

### <span data-ttu-id="e5d6f-116">Exemplo 3: Criar ponto de extremidade privado para ASEv3</span><span class="sxs-lookup"><span data-stu-id="e5d6f-116">Example 3: Create private endpoint for ASEv3</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironmentInboundServices -ResourceGroupName AseResourceGroup -Name AseV2Name
-VirtualNetworkName MyVirtualNetwork -SubnetName InboundSubnet -SkipDns
```

<span data-ttu-id="e5d6f-117">Criar ponto de extremidade privado para ASEv3</span><span class="sxs-lookup"><span data-stu-id="e5d6f-117">Create private endpoint for ASEv3</span></span>

## <span data-ttu-id="e5d6f-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e5d6f-118">PARAMETERS</span></span>

### <span data-ttu-id="e5d6f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5d6f-119">-DefaultProfile</span></span>
<span data-ttu-id="e5d6f-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e5d6f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5d6f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e5d6f-121">-Name</span></span>
<span data-ttu-id="e5d6f-122">O nome do ambiente de serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e5d6f-122">The name of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5d6f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5d6f-123">-PassThru</span></span>
<span data-ttu-id="e5d6f-124">Status de retorno.</span><span class="sxs-lookup"><span data-stu-id="e5d6f-124">Return status.</span></span>

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

### <span data-ttu-id="e5d6f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5d6f-125">-ResourceGroupName</span></span>
<span data-ttu-id="e5d6f-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e5d6f-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5d6f-127">-SkipDns</span><span class="sxs-lookup"><span data-stu-id="e5d6f-127">-SkipDns</span></span>
<span data-ttu-id="e5d6f-128">Não crie registros e zona DNS privada do Azure.</span><span class="sxs-lookup"><span data-stu-id="e5d6f-128">Do not create Azure Private DNS Zone and records.</span></span>

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

### <span data-ttu-id="e5d6f-129">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="e5d6f-129">-SubnetId</span></span>
<span data-ttu-id="e5d6f-130">A id da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="e5d6f-130">The subnet id.</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5d6f-131">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="e5d6f-131">-SubnetName</span></span>
<span data-ttu-id="e5d6f-132">O nome da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="e5d6f-132">The subnet name.</span></span> <span data-ttu-id="e5d6f-133">Usado em combinação com -VirtualNetworkName e deve estar no mesmo grupo de recursos que o ASE.</span><span class="sxs-lookup"><span data-stu-id="e5d6f-133">Used in combination with -VirtualNetworkName and must be in same resource group as ASE.</span></span> <span data-ttu-id="e5d6f-134">Caso não seja, use -SubnetId</span><span class="sxs-lookup"><span data-stu-id="e5d6f-134">If not, use -SubnetId</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5d6f-135">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="e5d6f-135">-VirtualNetworkName</span></span>
<span data-ttu-id="e5d6f-136">O nome da vNet.</span><span class="sxs-lookup"><span data-stu-id="e5d6f-136">The vNet name.</span></span> <span data-ttu-id="e5d6f-137">Usado em combinação com -SubnetName e deve estar no mesmo grupo de recursos que o ASE.</span><span class="sxs-lookup"><span data-stu-id="e5d6f-137">Used in combination with -SubnetName and must be in same resource group as ASE.</span></span> <span data-ttu-id="e5d6f-138">Caso não seja, use -SubnetId</span><span class="sxs-lookup"><span data-stu-id="e5d6f-138">If not, use -SubnetId</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5d6f-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5d6f-139">-Confirm</span></span>
<span data-ttu-id="e5d6f-140">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5d6f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5d6f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5d6f-141">-WhatIf</span></span>
<span data-ttu-id="e5d6f-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e5d6f-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5d6f-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e5d6f-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5d6f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5d6f-144">CommonParameters</span></span>
<span data-ttu-id="e5d6f-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5d6f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5d6f-146">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5d6f-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5d6f-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5d6f-147">INPUTS</span></span>

### <span data-ttu-id="e5d6f-148">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e5d6f-148">None</span></span>

## <span data-ttu-id="e5d6f-149">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e5d6f-149">OUTPUTS</span></span>

### <span data-ttu-id="e5d6f-150">System.Object</span><span class="sxs-lookup"><span data-stu-id="e5d6f-150">System.Object</span></span>
## <span data-ttu-id="e5d6f-151">NOTES</span><span class="sxs-lookup"><span data-stu-id="e5d6f-151">NOTES</span></span>

## <span data-ttu-id="e5d6f-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5d6f-152">RELATED LINKS</span></span>

[<span data-ttu-id="e5d6f-153">New-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="e5d6f-153">New-AzAppServiceEnvironment</span></span>](./New-AzAppServiceEnvironment.md)

[<span data-ttu-id="e5d6f-154">Get-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="e5d6f-154">Get-AzAppServiceEnvironment</span></span>](./Get-AzAppServiceEnvironment.md)

[<span data-ttu-id="e5d6f-155">Remove-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="e5d6f-155">Remove-AzAppServiceEnvironment</span></span>](./Remove-AzAppServiceEnvironment.md)