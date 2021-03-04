---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/new-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwarePrivateCloud.md
ms.openlocfilehash: 8cdc8e49a78c4f2c2bfb88d42fe710ad783df97f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890043"
---
# <span data-ttu-id="091cc-101">New-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="091cc-101">New-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="091cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="091cc-102">SYNOPSIS</span></span>
<span data-ttu-id="091cc-103">Criar ou atualizar uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="091cc-103">Create or update a private cloud</span></span>

## <span data-ttu-id="091cc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="091cc-104">SYNTAX</span></span>

```
New-AzVMwarePrivateCloud -Name <String> -ResourceGroupName <String> -Location <String>
 -ManagementClusterSize <Int32> -NetworkBlock <String> -Sku <String> [-SubscriptionId <String>] [-AcceptEULA]
 [-Internet <InternetEnum>] [-NsxtPassword <String>] [-Tag <Hashtable>] [-VcenterPassword <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="091cc-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="091cc-105">DESCRIPTION</span></span>
<span data-ttu-id="091cc-106">Criar ou atualizar uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="091cc-106">Create or update a private cloud</span></span>

## <span data-ttu-id="091cc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="091cc-107">EXAMPLES</span></span>

### <span data-ttu-id="091cc-108">Exemplo 1: Criar nuvem privada</span><span class="sxs-lookup"><span data-stu-id="091cc-108">Example 1: Create private cloud</span></span>
```powershell
PS C:\> New-AzVMWarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -NetworkBlock 192.168.48.0/22 -SkuName av36 -ManagementClusterSize 3 -Location australiaeast

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="091cc-109">Criar nuvem privada</span><span class="sxs-lookup"><span data-stu-id="091cc-109">Create private cloud</span></span>

## <span data-ttu-id="091cc-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="091cc-110">PARAMETERS</span></span>

### <span data-ttu-id="091cc-111">-AcceptEULA</span><span class="sxs-lookup"><span data-stu-id="091cc-111">-AcceptEULA</span></span>
<span data-ttu-id="091cc-112">Aceitar a EULA do AVS, o termo legal será pop-up sem esse parâmetro fornecido</span><span class="sxs-lookup"><span data-stu-id="091cc-112">Accept EULA of AVS, legal term will pop up without this parameter provided</span></span>

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

### <span data-ttu-id="091cc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="091cc-113">-AsJob</span></span>
<span data-ttu-id="091cc-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="091cc-114">Run the command as a job</span></span>

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

### <span data-ttu-id="091cc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="091cc-115">-DefaultProfile</span></span>
<span data-ttu-id="091cc-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="091cc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="091cc-117">-Internet</span><span class="sxs-lookup"><span data-stu-id="091cc-117">-Internet</span></span>
<span data-ttu-id="091cc-118">A conectividade com a Internet está habilitada ou desabilitada</span><span class="sxs-lookup"><span data-stu-id="091cc-118">Connectivity to internet is enabled or disabled</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Support.InternetEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="091cc-119">-Location</span><span class="sxs-lookup"><span data-stu-id="091cc-119">-Location</span></span>
<span data-ttu-id="091cc-120">Local do recurso</span><span class="sxs-lookup"><span data-stu-id="091cc-120">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="091cc-121">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="091cc-121">-ManagementClusterSize</span></span>
<span data-ttu-id="091cc-122">O tamanho do cluster</span><span class="sxs-lookup"><span data-stu-id="091cc-122">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="091cc-123">-Name</span><span class="sxs-lookup"><span data-stu-id="091cc-123">-Name</span></span>
<span data-ttu-id="091cc-124">Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="091cc-124">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="091cc-125">-NetworkBlock</span><span class="sxs-lookup"><span data-stu-id="091cc-125">-NetworkBlock</span></span>
<span data-ttu-id="091cc-126">O bloco de endereços deve ser exclusivo na VNet em sua assinatura, bem como no local.</span><span class="sxs-lookup"><span data-stu-id="091cc-126">The block of addresses should be unique across VNet in your subscription as well as on-premise.</span></span>
<span data-ttu-id="091cc-127">Certifique-se de que o formato CIDR está conformed com (A.B.C.D/X) onde A,B,C,D estão entre 0 e 255 e X está entre 0 e 22</span><span class="sxs-lookup"><span data-stu-id="091cc-127">Make sure the CIDR format is conformed to (A.B.C.D/X) where A,B,C,D are between 0 and 255, and X is between 0 and 22</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="091cc-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="091cc-128">-NoWait</span></span>
<span data-ttu-id="091cc-129">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="091cc-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="091cc-130">-NsxtPassword</span><span class="sxs-lookup"><span data-stu-id="091cc-130">-NsxtPassword</span></span>
<span data-ttu-id="091cc-131">Opcionalmente, de definir a senha do NSX-T Manager quando a nuvem privada for criada</span><span class="sxs-lookup"><span data-stu-id="091cc-131">Optionally, set the NSX-T Manager password when the private cloud is created</span></span>

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

### <span data-ttu-id="091cc-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="091cc-132">-ResourceGroupName</span></span>
<span data-ttu-id="091cc-133">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="091cc-133">The name of the resource group.</span></span>
<span data-ttu-id="091cc-134">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="091cc-134">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="091cc-135">-Sku</span><span class="sxs-lookup"><span data-stu-id="091cc-135">-Sku</span></span>
<span data-ttu-id="091cc-136">O nome da SKU.</span><span class="sxs-lookup"><span data-stu-id="091cc-136">The name of the SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="091cc-137">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="091cc-137">-SubscriptionId</span></span>
<span data-ttu-id="091cc-138">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="091cc-138">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="091cc-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="091cc-139">-Tag</span></span>
<span data-ttu-id="091cc-140">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="091cc-140">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="091cc-141">-VcenterPassword</span><span class="sxs-lookup"><span data-stu-id="091cc-141">-VcenterPassword</span></span>
<span data-ttu-id="091cc-142">Opcionalmente, de definir a senha de administrador do vCenter quando a nuvem privada for criada</span><span class="sxs-lookup"><span data-stu-id="091cc-142">Optionally, set the vCenter admin password when the private cloud is created</span></span>

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

### <span data-ttu-id="091cc-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="091cc-143">-Confirm</span></span>
<span data-ttu-id="091cc-144">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="091cc-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="091cc-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="091cc-145">-WhatIf</span></span>
<span data-ttu-id="091cc-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="091cc-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="091cc-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="091cc-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="091cc-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="091cc-148">CommonParameters</span></span>
<span data-ttu-id="091cc-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="091cc-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="091cc-150">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="091cc-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="091cc-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="091cc-151">INPUTS</span></span>

## <span data-ttu-id="091cc-152">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="091cc-152">OUTPUTS</span></span>

### <span data-ttu-id="091cc-153">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="091cc-153">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="091cc-154">NOTES</span><span class="sxs-lookup"><span data-stu-id="091cc-154">NOTES</span></span>

<span data-ttu-id="091cc-155">ALIASES</span><span class="sxs-lookup"><span data-stu-id="091cc-155">ALIASES</span></span>

## <span data-ttu-id="091cc-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="091cc-156">RELATED LINKS</span></span>

