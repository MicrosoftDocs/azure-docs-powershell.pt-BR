---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.VMware/new-azVMwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwarePrivateCloud.md
ms.openlocfilehash: 3e5e8fa4d098ce68899294a25866b4636c80878e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113899"
---
# <span data-ttu-id="a09bb-101">New-AzVMwarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="a09bb-101">New-AzVMwarePrivateCloud</span></span>

## <span data-ttu-id="a09bb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a09bb-102">SYNOPSIS</span></span>
<span data-ttu-id="a09bb-103">Criar ou atualizar uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="a09bb-103">Create or update a private cloud</span></span>

## <span data-ttu-id="a09bb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a09bb-104">SYNTAX</span></span>

```
New-AzVMwarePrivateCloud -Name <String> -ResourceGroupName <String> -Location <String>
 -ManagementClusterSize <Int32> -NetworkBlock <String> -Sku <String> [-SubscriptionId <String>] [-AcceptEULA]
 [-Internet <InternetEnum>] [-NsxtPassword <String>] [-Tag <Hashtable>] [-VcenterPassword <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a09bb-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="a09bb-105">DESCRIPTION</span></span>
<span data-ttu-id="a09bb-106">Criar ou atualizar uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="a09bb-106">Create or update a private cloud</span></span>

## <span data-ttu-id="a09bb-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a09bb-107">EXAMPLES</span></span>

### <span data-ttu-id="a09bb-108">Exemplo 1: Criar nuvem privada</span><span class="sxs-lookup"><span data-stu-id="a09bb-108">Example 1: Create private cloud</span></span>
```powershell
PS C:\> New-AzVMwarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -NetworkBlock 192.168.48.0/22 -SkuName av36 -ManagementClusterSize 3 -Location australiaeast

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="a09bb-109">Criar nuvem privada</span><span class="sxs-lookup"><span data-stu-id="a09bb-109">Create private cloud</span></span>

## <span data-ttu-id="a09bb-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a09bb-110">PARAMETERS</span></span>

### <span data-ttu-id="a09bb-111">-AcceptEULA</span><span class="sxs-lookup"><span data-stu-id="a09bb-111">-AcceptEULA</span></span>
<span data-ttu-id="a09bb-112">Aceitar a EULA do AVS, o termo legal será disponibilizado sem este parâmetro fornecido</span><span class="sxs-lookup"><span data-stu-id="a09bb-112">Accept EULA of AVS, legal term will pop up without this parameter provided</span></span>

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

### <span data-ttu-id="a09bb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a09bb-113">-AsJob</span></span>
<span data-ttu-id="a09bb-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="a09bb-114">Run the command as a job</span></span>

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

### <span data-ttu-id="a09bb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a09bb-115">-DefaultProfile</span></span>
<span data-ttu-id="a09bb-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a09bb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a09bb-117">-Internet</span><span class="sxs-lookup"><span data-stu-id="a09bb-117">-Internet</span></span>
<span data-ttu-id="a09bb-118">A conectividade com a Internet está habilitada ou desabilitada</span><span class="sxs-lookup"><span data-stu-id="a09bb-118">Connectivity to internet is enabled or disabled</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Support.InternetEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a09bb-119">-Local</span><span class="sxs-lookup"><span data-stu-id="a09bb-119">-Location</span></span>
<span data-ttu-id="a09bb-120">Local do recurso</span><span class="sxs-lookup"><span data-stu-id="a09bb-120">Resource location</span></span>

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

### <span data-ttu-id="a09bb-121">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="a09bb-121">-ManagementClusterSize</span></span>
<span data-ttu-id="a09bb-122">O tamanho do cluster</span><span class="sxs-lookup"><span data-stu-id="a09bb-122">The cluster size</span></span>

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

### <span data-ttu-id="a09bb-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="a09bb-123">-Name</span></span>
<span data-ttu-id="a09bb-124">Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="a09bb-124">Name of the private cloud</span></span>

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

### <span data-ttu-id="a09bb-125">-NetworkBlock</span><span class="sxs-lookup"><span data-stu-id="a09bb-125">-NetworkBlock</span></span>
<span data-ttu-id="a09bb-126">O bloco de endereços deve ser exclusivo na VNet em sua assinatura, bem como no local.</span><span class="sxs-lookup"><span data-stu-id="a09bb-126">The block of addresses should be unique across VNet in your subscription as well as on-premise.</span></span>
<span data-ttu-id="a09bb-127">Certifique-se de que o formato CIDR está conforme (A.B.C.D/X) em que A,B,C,D está entre 0 e 255 e X está entre 0 e 22</span><span class="sxs-lookup"><span data-stu-id="a09bb-127">Make sure the CIDR format is conformed to (A.B.C.D/X) where A,B,C,D are between 0 and 255, and X is between 0 and 22</span></span>

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

### <span data-ttu-id="a09bb-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a09bb-128">-NoWait</span></span>
<span data-ttu-id="a09bb-129">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="a09bb-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a09bb-130">-NsxtPassword</span><span class="sxs-lookup"><span data-stu-id="a09bb-130">-NsxtPassword</span></span>
<span data-ttu-id="a09bb-131">Opcionalmente, de definir a senha do NSX-T Manager quando a nuvem privada for criada</span><span class="sxs-lookup"><span data-stu-id="a09bb-131">Optionally, set the NSX-T Manager password when the private cloud is created</span></span>

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

### <span data-ttu-id="a09bb-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a09bb-132">-ResourceGroupName</span></span>
<span data-ttu-id="a09bb-133">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a09bb-133">The name of the resource group.</span></span>
<span data-ttu-id="a09bb-134">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a09bb-134">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a09bb-135">-SKU</span><span class="sxs-lookup"><span data-stu-id="a09bb-135">-Sku</span></span>
<span data-ttu-id="a09bb-136">O nome da SKU.</span><span class="sxs-lookup"><span data-stu-id="a09bb-136">The name of the SKU.</span></span>

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

### <span data-ttu-id="a09bb-137">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a09bb-137">-SubscriptionId</span></span>
<span data-ttu-id="a09bb-138">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="a09bb-138">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a09bb-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="a09bb-139">-Tag</span></span>
<span data-ttu-id="a09bb-140">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="a09bb-140">Resource tags</span></span>

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

### <span data-ttu-id="a09bb-141">-VcenterPassword</span><span class="sxs-lookup"><span data-stu-id="a09bb-141">-VcenterPassword</span></span>
<span data-ttu-id="a09bb-142">Opcionalmente, de definir a senha de administrador do vCenter quando a nuvem particular for criada</span><span class="sxs-lookup"><span data-stu-id="a09bb-142">Optionally, set the vCenter admin password when the private cloud is created</span></span>

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

### <span data-ttu-id="a09bb-143">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a09bb-143">-Confirm</span></span>
<span data-ttu-id="a09bb-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a09bb-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a09bb-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a09bb-145">-WhatIf</span></span>
<span data-ttu-id="a09bb-146">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a09bb-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a09bb-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a09bb-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a09bb-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a09bb-148">CommonParameters</span></span>
<span data-ttu-id="a09bb-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a09bb-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a09bb-150">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a09bb-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a09bb-151">Entradas</span><span class="sxs-lookup"><span data-stu-id="a09bb-151">INPUTS</span></span>

## <span data-ttu-id="a09bb-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="a09bb-152">OUTPUTS</span></span>

### <span data-ttu-id="a09bb-153">Microsoft.Azure.PowerShell.Cmdlets.VCloud.Models.Api20200320.IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="a09bb-153">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="a09bb-154">Notas</span><span class="sxs-lookup"><span data-stu-id="a09bb-154">NOTES</span></span>

<span data-ttu-id="a09bb-155">Aliases</span><span class="sxs-lookup"><span data-stu-id="a09bb-155">ALIASES</span></span>

## <span data-ttu-id="a09bb-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a09bb-156">RELATED LINKS</span></span>

