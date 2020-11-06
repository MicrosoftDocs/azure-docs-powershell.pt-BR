---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
ms.openlocfilehash: 9d6614204c8c6e8e95617ed989e3f75b88c9744e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597374"
---
# <span data-ttu-id="3a718-101">New-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="3a718-101">New-AzHostGroup</span></span>

## <span data-ttu-id="3a718-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3a718-102">SYNOPSIS</span></span>
<span data-ttu-id="3a718-103">Cria um grupo de hosts.</span><span class="sxs-lookup"><span data-stu-id="3a718-103">Creates a host group.</span></span>

## <span data-ttu-id="3a718-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a718-104">SYNTAX</span></span>

```
New-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 -PlatformFaultDomain <Int32> [-Zone <String[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a718-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3a718-105">DESCRIPTION</span></span>
<span data-ttu-id="3a718-106">Esse cmdlet criará um grupo de hosts.</span><span class="sxs-lookup"><span data-stu-id="3a718-106">This cmdlet will create a Host group.</span></span>

## <span data-ttu-id="3a718-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3a718-107">EXAMPLES</span></span>

### <span data-ttu-id="3a718-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3a718-108">Example 1</span></span>
```
PS C:\> New-AzHostGroup -ResourceGroupName $resourceGroupName -Name $hostGroupName -Location $location -Zone $zone

ResourceGroupName        : myrg01
PlatformFaultDomainCount : 2
Hosts                    : {/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01}
Zones                    : {1}
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01
Name                     : myhostgroup01
Location                 : eastus
Tags                     : {[key1, val1]}
```

<span data-ttu-id="3a718-109">Esse comando cria um grupo de hosts no local e na zona especificados.</span><span class="sxs-lookup"><span data-stu-id="3a718-109">This command creates a host group in the given location and zone.</span></span>

## <span data-ttu-id="3a718-110">OS</span><span class="sxs-lookup"><span data-stu-id="3a718-110">PARAMETERS</span></span>

### <span data-ttu-id="3a718-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a718-111">-AsJob</span></span>
<span data-ttu-id="3a718-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3a718-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3a718-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a718-113">-DefaultProfile</span></span>
<span data-ttu-id="3a718-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3a718-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a718-115">-Local</span><span class="sxs-lookup"><span data-stu-id="3a718-115">-Location</span></span>
<span data-ttu-id="3a718-116">Especifica o local.</span><span class="sxs-lookup"><span data-stu-id="3a718-116">Specifies location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a718-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="3a718-117">-Name</span></span>
<span data-ttu-id="3a718-118">Especifica o nome do grupo host.</span><span class="sxs-lookup"><span data-stu-id="3a718-118">Specifies the name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HostGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a718-119">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="3a718-119">-PlatformFaultDomain</span></span>
<span data-ttu-id="3a718-120">Especifica o número de domínios de falha que o grupo de hosts pode abranger.</span><span class="sxs-lookup"><span data-stu-id="3a718-120">Specifies the number of fault domains that the host group can span.</span></span>  <span data-ttu-id="3a718-121">O valor mínimo é 1 e o valor máximo é 3.</span><span class="sxs-lookup"><span data-stu-id="3a718-121">The minimum value is 1 and the maximum value is 3.</span></span>

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

### <span data-ttu-id="3a718-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a718-122">-ResourceGroupName</span></span>
<span data-ttu-id="3a718-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3a718-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="3a718-124">-Marca</span><span class="sxs-lookup"><span data-stu-id="3a718-124">-Tag</span></span>
<span data-ttu-id="3a718-125">Especifica marcas</span><span class="sxs-lookup"><span data-stu-id="3a718-125">Specifies Tags</span></span>

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

### <span data-ttu-id="3a718-126">-Zone</span><span class="sxs-lookup"><span data-stu-id="3a718-126">-Zone</span></span>
<span data-ttu-id="3a718-127">Especifica zonas do grupo host.</span><span class="sxs-lookup"><span data-stu-id="3a718-127">Specifies Zones of the host group.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a718-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3a718-128">-Confirm</span></span>
<span data-ttu-id="3a718-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a718-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a718-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a718-130">-WhatIf</span></span>
<span data-ttu-id="3a718-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3a718-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a718-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3a718-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a718-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a718-133">CommonParameters</span></span>
<span data-ttu-id="3a718-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a718-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a718-135">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a718-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a718-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3a718-136">INPUTS</span></span>

### <span data-ttu-id="3a718-137">System. String</span><span class="sxs-lookup"><span data-stu-id="3a718-137">System.String</span></span>

## <span data-ttu-id="3a718-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3a718-138">OUTPUTS</span></span>

### <span data-ttu-id="3a718-139">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="3a718-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="3a718-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3a718-140">NOTES</span></span>

## <span data-ttu-id="3a718-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3a718-141">RELATED LINKS</span></span>
