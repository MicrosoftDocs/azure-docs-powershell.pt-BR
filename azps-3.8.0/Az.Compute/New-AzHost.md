---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHost.md
ms.openlocfilehash: 58ae996e4d2723d4b38b548dd8225a2a483ce8f7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941461"
---
# <span data-ttu-id="70a87-101">New-AzHost</span><span class="sxs-lookup"><span data-stu-id="70a87-101">New-AzHost</span></span>

## <span data-ttu-id="70a87-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="70a87-102">SYNOPSIS</span></span>
<span data-ttu-id="70a87-103">Cria um host.</span><span class="sxs-lookup"><span data-stu-id="70a87-103">Creates a  host.</span></span>

## <span data-ttu-id="70a87-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="70a87-104">SYNTAX</span></span>

```
New-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-Location] <String>
 -Sku <String> [-PlatformFaultDomain <Int32>] [-AutoReplaceOnFailure <Boolean>]
 [-LicenseType <DedicatedHostLicenseTypes>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70a87-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="70a87-105">DESCRIPTION</span></span>
<span data-ttu-id="70a87-106">Esse cmdlet criará um host.</span><span class="sxs-lookup"><span data-stu-id="70a87-106">This cmdlet will create a Host.</span></span>

## <span data-ttu-id="70a87-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="70a87-107">EXAMPLES</span></span>

### <span data-ttu-id="70a87-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="70a87-108">Example 1</span></span>
```
PS C:\> New-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName -Location $location -Sku $skuName

ResourceGroupName    : myrg01
PlatformFaultDomain  : 0
AutoReplaceOnFailure : True
HostId               : 00000000-0000-0000-0000-000000000000
ProvisioningTime     : 7/25/2019 8:34:16 PM
ProvisioningState    : Succeeded
Sku                  : 
  Name               : ESv3-Type1
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01
Name                 : myhost01
Location             : eastus
Tags                 : {"key1":"val2"}
```

<span data-ttu-id="70a87-109">Esse comando cria um host da SKU fornecida no grupo host fornecido e o local indicado.</span><span class="sxs-lookup"><span data-stu-id="70a87-109">This command creates a host of the given Sku in the given host group and the given location.</span></span>

## <span data-ttu-id="70a87-110">OS</span><span class="sxs-lookup"><span data-stu-id="70a87-110">PARAMETERS</span></span>

### <span data-ttu-id="70a87-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70a87-111">-AsJob</span></span>
<span data-ttu-id="70a87-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="70a87-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="70a87-113">-AutoReplaceOnFailure</span><span class="sxs-lookup"><span data-stu-id="70a87-113">-AutoReplaceOnFailure</span></span>
<span data-ttu-id="70a87-114">Especifica se o host deve ser substituído automaticamente em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="70a87-114">Specifies whether the host should be replaced automatically in case of a failure.</span></span> <span data-ttu-id="70a87-115">O valor padrão é "true" quando não é fornecido.</span><span class="sxs-lookup"><span data-stu-id="70a87-115">The value is defaulted to 'true' when not provided.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70a87-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70a87-116">-DefaultProfile</span></span>
<span data-ttu-id="70a87-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="70a87-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70a87-118">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="70a87-118">-HostGroupName</span></span>
<span data-ttu-id="70a87-119">Especifica o nome do grupo host.</span><span class="sxs-lookup"><span data-stu-id="70a87-119">Specifies the name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70a87-120">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="70a87-120">-LicenseType</span></span>
<span data-ttu-id="70a87-121">Especifica o tipo de licença de software que será aplicado às VMs implantadas no host.</span><span class="sxs-lookup"><span data-stu-id="70a87-121">Specifies the software license type that will be applied to the VMs deployed on the host.</span></span> <span data-ttu-id="70a87-122">Os valores possíveis são: None, Windows_Server_Hybrid e Windows_Server_Perpetual.</span><span class="sxs-lookup"><span data-stu-id="70a87-122">Possible values are: None, Windows_Server_Hybrid, and Windows_Server_Perpetual.</span></span>  <span data-ttu-id="70a87-123">O valor padrão é nenhum.</span><span class="sxs-lookup"><span data-stu-id="70a87-123">Default value is None.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.DedicatedHostLicenseTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, WindowsServerHybrid, WindowsServerPerpetual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70a87-124">-Local</span><span class="sxs-lookup"><span data-stu-id="70a87-124">-Location</span></span>
<span data-ttu-id="70a87-125">Especifica o local.</span><span class="sxs-lookup"><span data-stu-id="70a87-125">Specifies the location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70a87-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="70a87-126">-Name</span></span>
<span data-ttu-id="70a87-127">Especifica o nome do host.</span><span class="sxs-lookup"><span data-stu-id="70a87-127">Specifies the name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70a87-128">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="70a87-128">-PlatformFaultDomain</span></span>
<span data-ttu-id="70a87-129">Especifica o número do domínio de falha da plataforma do host.</span><span class="sxs-lookup"><span data-stu-id="70a87-129">Specifies the number of platform fault domain of the host.</span></span>  <span data-ttu-id="70a87-130">Em seguida, o valor mínimo é 0 e o valor máximo é 2.</span><span class="sxs-lookup"><span data-stu-id="70a87-130">Then minimum value is 0 and the maximum value is 2.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70a87-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70a87-131">-ResourceGroupName</span></span>
<span data-ttu-id="70a87-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="70a87-132">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70a87-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="70a87-133">-Sku</span></span>
<span data-ttu-id="70a87-134">Especifica o nome do SKU.</span><span class="sxs-lookup"><span data-stu-id="70a87-134">Specifies the name of the SKU.</span></span>

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

### <span data-ttu-id="70a87-135">-Marca</span><span class="sxs-lookup"><span data-stu-id="70a87-135">-Tag</span></span>
<span data-ttu-id="70a87-136">Especifica marcas.</span><span class="sxs-lookup"><span data-stu-id="70a87-136">Specifies Tags.</span></span>

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

### <span data-ttu-id="70a87-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="70a87-137">-Confirm</span></span>
<span data-ttu-id="70a87-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70a87-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70a87-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70a87-139">-WhatIf</span></span>
<span data-ttu-id="70a87-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="70a87-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70a87-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="70a87-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70a87-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70a87-142">CommonParameters</span></span>
<span data-ttu-id="70a87-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70a87-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70a87-144">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70a87-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70a87-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="70a87-145">INPUTS</span></span>

### <span data-ttu-id="70a87-146">System. String</span><span class="sxs-lookup"><span data-stu-id="70a87-146">System.String</span></span>

## <span data-ttu-id="70a87-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="70a87-147">OUTPUTS</span></span>

### <span data-ttu-id="70a87-148">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSHost</span><span class="sxs-lookup"><span data-stu-id="70a87-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="70a87-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="70a87-149">NOTES</span></span>

## <span data-ttu-id="70a87-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="70a87-150">RELATED LINKS</span></span>
