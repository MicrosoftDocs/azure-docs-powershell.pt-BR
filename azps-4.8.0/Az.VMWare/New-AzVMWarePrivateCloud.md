---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWarePrivateCloud.md
ms.openlocfilehash: 5dd91db9a8141bf9992da9eb364b00301036a898
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113437"
---
# <span data-ttu-id="39d72-101">New-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="39d72-101">New-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="39d72-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="39d72-102">SYNOPSIS</span></span>
<span data-ttu-id="39d72-103">Criar ou atualizar uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="39d72-103">Create or update a private cloud</span></span>

## <span data-ttu-id="39d72-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="39d72-104">SYNTAX</span></span>

```
New-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> -Location <String>
 -ManagementClusterSize <Int32> -NetworkBlock <String> -Sku <String> [-SubscriptionId <String>]
 [-Internet <InternetEnum>] [-NsxtPassword <String>] [-Tag <Hashtable>] [-VcenterPassword <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="39d72-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="39d72-105">DESCRIPTION</span></span>
<span data-ttu-id="39d72-106">Criar ou atualizar uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="39d72-106">Create or update a private cloud</span></span>

## <span data-ttu-id="39d72-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="39d72-107">EXAMPLES</span></span>

### <span data-ttu-id="39d72-108">Exemplo 1: criar nuvem privada</span><span class="sxs-lookup"><span data-stu-id="39d72-108">Example 1: Create private cloud</span></span>
```powershell
PS C:\> New-AzVMWarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -NetworkBlock 192.168.48.0/22 -SkuName av36 -ManagementClusterSize 3 -Location australiaeast

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="39d72-109">Criar nuvem privada</span><span class="sxs-lookup"><span data-stu-id="39d72-109">Create private cloud</span></span>

## <span data-ttu-id="39d72-110">OS</span><span class="sxs-lookup"><span data-stu-id="39d72-110">PARAMETERS</span></span>

### <span data-ttu-id="39d72-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39d72-111">-AsJob</span></span>
<span data-ttu-id="39d72-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="39d72-112">Run the command as a job</span></span>

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

### <span data-ttu-id="39d72-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39d72-113">-DefaultProfile</span></span>
<span data-ttu-id="39d72-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="39d72-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39d72-115">-Internet</span><span class="sxs-lookup"><span data-stu-id="39d72-115">-Internet</span></span>
<span data-ttu-id="39d72-116">A conectividade com a Internet está habilitada ou desabilitada</span><span class="sxs-lookup"><span data-stu-id="39d72-116">Connectivity to internet is enabled or disabled</span></span>

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

### <span data-ttu-id="39d72-117">-Local</span><span class="sxs-lookup"><span data-stu-id="39d72-117">-Location</span></span>
<span data-ttu-id="39d72-118">Local do recurso</span><span class="sxs-lookup"><span data-stu-id="39d72-118">Resource location</span></span>

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

### <span data-ttu-id="39d72-119">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="39d72-119">-ManagementClusterSize</span></span>
<span data-ttu-id="39d72-120">O tamanho do cluster</span><span class="sxs-lookup"><span data-stu-id="39d72-120">The cluster size</span></span>

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

### <span data-ttu-id="39d72-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="39d72-121">-Name</span></span>
<span data-ttu-id="39d72-122">Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="39d72-122">Name of the private cloud</span></span>

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

### <span data-ttu-id="39d72-123">-NetworkBlock</span><span class="sxs-lookup"><span data-stu-id="39d72-123">-NetworkBlock</span></span>
<span data-ttu-id="39d72-124">O bloco de endereços deve ser exclusivo na VNet na sua assinatura e no local.</span><span class="sxs-lookup"><span data-stu-id="39d72-124">The block of addresses should be unique across VNet in your subscription as well as on-premise.</span></span>
<span data-ttu-id="39d72-125">Verifique se o formato CIDR está conforme o (A. B. C. D/X) em que A, B, C, D estão entre 0 e 255 e X está entre 0 e 22</span><span class="sxs-lookup"><span data-stu-id="39d72-125">Make sure the CIDR format is conformed to (A.B.C.D/X) where A,B,C,D are between 0 and 255, and X is between 0 and 22</span></span>

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

### <span data-ttu-id="39d72-126">-Nowait</span><span class="sxs-lookup"><span data-stu-id="39d72-126">-NoWait</span></span>
<span data-ttu-id="39d72-127">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="39d72-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="39d72-128">-NsxtPassword</span><span class="sxs-lookup"><span data-stu-id="39d72-128">-NsxtPassword</span></span>
<span data-ttu-id="39d72-129">Opcionalmente, defina a senha do NSX-T Manager quando a nuvem privada for criada</span><span class="sxs-lookup"><span data-stu-id="39d72-129">Optionally, set the NSX-T Manager password when the private cloud is created</span></span>

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

### <span data-ttu-id="39d72-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39d72-130">-ResourceGroupName</span></span>
<span data-ttu-id="39d72-131">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="39d72-131">The name of the resource group.</span></span>
<span data-ttu-id="39d72-132">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="39d72-132">The name is case insensitive.</span></span>

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

### <span data-ttu-id="39d72-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="39d72-133">-Sku</span></span>
<span data-ttu-id="39d72-134">O nome da SKU.</span><span class="sxs-lookup"><span data-stu-id="39d72-134">The name of the SKU.</span></span>

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

### <span data-ttu-id="39d72-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="39d72-135">-SubscriptionId</span></span>
<span data-ttu-id="39d72-136">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="39d72-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="39d72-137">-Marca</span><span class="sxs-lookup"><span data-stu-id="39d72-137">-Tag</span></span>
<span data-ttu-id="39d72-138">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="39d72-138">Resource tags</span></span>

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

### <span data-ttu-id="39d72-139">-VcenterPassword</span><span class="sxs-lookup"><span data-stu-id="39d72-139">-VcenterPassword</span></span>
<span data-ttu-id="39d72-140">Opcionalmente, defina a senha do administrador do vCenter quando a nuvem privada for criada</span><span class="sxs-lookup"><span data-stu-id="39d72-140">Optionally, set the vCenter admin password when the private cloud is created</span></span>

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

### <span data-ttu-id="39d72-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="39d72-141">-Confirm</span></span>
<span data-ttu-id="39d72-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39d72-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39d72-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39d72-143">-WhatIf</span></span>
<span data-ttu-id="39d72-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="39d72-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39d72-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="39d72-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39d72-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39d72-146">CommonParameters</span></span>
<span data-ttu-id="39d72-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39d72-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39d72-148">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39d72-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39d72-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="39d72-149">INPUTS</span></span>

## <span data-ttu-id="39d72-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="39d72-150">OUTPUTS</span></span>

### <span data-ttu-id="39d72-151">Microsoft. Azure. PowerShell. cmdlets. VMWare. Models. Api20200320. IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="39d72-151">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="39d72-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="39d72-152">NOTES</span></span>

<span data-ttu-id="39d72-153">ALIASES</span><span class="sxs-lookup"><span data-stu-id="39d72-153">ALIASES</span></span>

## <span data-ttu-id="39d72-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="39d72-154">RELATED LINKS</span></span>

