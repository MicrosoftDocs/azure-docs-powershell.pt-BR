---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHost.md
ms.openlocfilehash: 58ae996e4d2723d4b38b548dd8225a2a483ce8f7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111141"
---
# <span data-ttu-id="f7d4b-101">New-AzHost</span><span class="sxs-lookup"><span data-stu-id="f7d4b-101">New-AzHost</span></span>

## <span data-ttu-id="f7d4b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f7d4b-102">SYNOPSIS</span></span>
<span data-ttu-id="f7d4b-103">Cria um host.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-103">Creates a  host.</span></span>

## <span data-ttu-id="f7d4b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f7d4b-104">SYNTAX</span></span>

```
New-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-Location] <String>
 -Sku <String> [-PlatformFaultDomain <Int32>] [-AutoReplaceOnFailure <Boolean>]
 [-LicenseType <DedicatedHostLicenseTypes>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7d4b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f7d4b-105">DESCRIPTION</span></span>
<span data-ttu-id="f7d4b-106">Este cmdlet criará um Host.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-106">This cmdlet will create a Host.</span></span>

## <span data-ttu-id="f7d4b-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f7d4b-107">EXAMPLES</span></span>

### <span data-ttu-id="f7d4b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f7d4b-108">Example 1</span></span>
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

<span data-ttu-id="f7d4b-109">Esse comando cria um host da SKU determinada no grupo de host determinado e no local determinado.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-109">This command creates a host of the given Sku in the given host group and the given location.</span></span>

## <span data-ttu-id="f7d4b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f7d4b-110">PARAMETERS</span></span>

### <span data-ttu-id="f7d4b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7d4b-111">-AsJob</span></span>
<span data-ttu-id="f7d4b-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f7d4b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f7d4b-113">-AutoReplaceOnFailure</span><span class="sxs-lookup"><span data-stu-id="f7d4b-113">-AutoReplaceOnFailure</span></span>
<span data-ttu-id="f7d4b-114">Especifica se o host deve ser substituído automaticamente em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-114">Specifies whether the host should be replaced automatically in case of a failure.</span></span> <span data-ttu-id="f7d4b-115">O valor é padrão para "verdadeiro" quando não é fornecido.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-115">The value is defaulted to 'true' when not provided.</span></span>

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

### <span data-ttu-id="f7d4b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7d4b-116">-DefaultProfile</span></span>
<span data-ttu-id="f7d4b-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7d4b-118">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="f7d4b-118">-HostGroupName</span></span>
<span data-ttu-id="f7d4b-119">Especifica o nome do grupo de host.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-119">Specifies the name of the host group.</span></span>

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

### <span data-ttu-id="f7d4b-120">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="f7d4b-120">-LicenseType</span></span>
<span data-ttu-id="f7d4b-121">Especifica o tipo de licença de software que será aplicado aos VMs implantados no host.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-121">Specifies the software license type that will be applied to the VMs deployed on the host.</span></span> <span data-ttu-id="f7d4b-122">Os valores possíveis são: Nenhum, Windows_Server_Hybrid e Windows_Server_Perpetual.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-122">Possible values are: None, Windows_Server_Hybrid, and Windows_Server_Perpetual.</span></span>  <span data-ttu-id="f7d4b-123">O valor padrão é Nenhum.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-123">Default value is None.</span></span>

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

### <span data-ttu-id="f7d4b-124">-Local</span><span class="sxs-lookup"><span data-stu-id="f7d4b-124">-Location</span></span>
<span data-ttu-id="f7d4b-125">Especifica o local.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-125">Specifies the location.</span></span>

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

### <span data-ttu-id="f7d4b-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="f7d4b-126">-Name</span></span>
<span data-ttu-id="f7d4b-127">Especifica o nome do host.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-127">Specifies the name of the host.</span></span>

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

### <span data-ttu-id="f7d4b-128">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="f7d4b-128">-PlatformFaultDomain</span></span>
<span data-ttu-id="f7d4b-129">Especifica o número de domínios de falha da plataforma do host.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-129">Specifies the number of platform fault domain of the host.</span></span>  <span data-ttu-id="f7d4b-130">Em seguida, o valor mínimo é 0 e o valor máximo é 2.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-130">Then minimum value is 0 and the maximum value is 2.</span></span>

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

### <span data-ttu-id="f7d4b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7d4b-131">-ResourceGroupName</span></span>
<span data-ttu-id="f7d4b-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="f7d4b-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="f7d4b-133">-Sku</span></span>
<span data-ttu-id="f7d4b-134">Especifica o nome da SKU.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-134">Specifies the name of the SKU.</span></span>

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

### <span data-ttu-id="f7d4b-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="f7d4b-135">-Tag</span></span>
<span data-ttu-id="f7d4b-136">Especifica marcas.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-136">Specifies Tags.</span></span>

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

### <span data-ttu-id="f7d4b-137">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f7d4b-137">-Confirm</span></span>
<span data-ttu-id="f7d4b-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7d4b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7d4b-139">-WhatIf</span></span>
<span data-ttu-id="f7d4b-140">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7d4b-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7d4b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7d4b-142">CommonParameters</span></span>
<span data-ttu-id="f7d4b-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7d4b-144">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7d4b-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7d4b-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="f7d4b-145">INPUTS</span></span>

### <span data-ttu-id="f7d4b-146">System.String</span><span class="sxs-lookup"><span data-stu-id="f7d4b-146">System.String</span></span>

## <span data-ttu-id="f7d4b-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="f7d4b-147">OUTPUTS</span></span>

### <span data-ttu-id="f7d4b-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span><span class="sxs-lookup"><span data-stu-id="f7d4b-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="f7d4b-149">Notas</span><span class="sxs-lookup"><span data-stu-id="f7d4b-149">NOTES</span></span>

## <span data-ttu-id="f7d4b-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f7d4b-150">RELATED LINKS</span></span>
