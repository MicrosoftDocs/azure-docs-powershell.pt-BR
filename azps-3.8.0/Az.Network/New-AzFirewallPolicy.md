---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
ms.openlocfilehash: 5c432224891de6c2fcadc42ae308e9607bc3e432
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777228"
---
# <span data-ttu-id="bff3e-101">New-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="bff3e-101">New-AzFirewallPolicy</span></span>

## <span data-ttu-id="bff3e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bff3e-102">SYNOPSIS</span></span>
<span data-ttu-id="bff3e-103">Cria uma nova política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="bff3e-103">Creates a new Azure Firewall Policy</span></span>

## <span data-ttu-id="bff3e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bff3e-104">SYNTAX</span></span>

```
New-AzFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String> [-ThreatIntelMode <String>]
 [-BasePolicy <String>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bff3e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bff3e-105">DESCRIPTION</span></span>
<span data-ttu-id="bff3e-106">O cmdlet **New-AzFirewallPolicy** cria uma política de firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="bff3e-106">The **New-AzFirewallPolicy** cmdlet creates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="bff3e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bff3e-107">EXAMPLES</span></span>

### <span data-ttu-id="bff3e-108">1. criar uma política vazia</span><span class="sxs-lookup"><span data-stu-id="bff3e-108">1. Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg
```

<span data-ttu-id="bff3e-109">Este exemplo cria uma política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="bff3e-109">This example creates an azure firewall policy</span></span>

### <span data-ttu-id="bff3e-110">2. criar uma política vazia com o modo ThreatIntel</span><span class="sxs-lookup"><span data-stu-id="bff3e-110">2. Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelMode "Deny"
```

<span data-ttu-id="bff3e-111">Este exemplo cria uma política de firewall do Azure com um modo de ameaça Intel</span><span class="sxs-lookup"><span data-stu-id="bff3e-111">This example creates an azure firewall policy with a threat intel mode</span></span>

## <span data-ttu-id="bff3e-112">OS</span><span class="sxs-lookup"><span data-stu-id="bff3e-112">PARAMETERS</span></span>

### <span data-ttu-id="bff3e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bff3e-113">-AsJob</span></span>
<span data-ttu-id="bff3e-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="bff3e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bff3e-115">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="bff3e-115">-BasePolicy</span></span>
<span data-ttu-id="bff3e-116">O modo de operação para inteligência de ameaças.</span><span class="sxs-lookup"><span data-stu-id="bff3e-116">The operation mode for Threat Intelligence.</span></span>

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

### <span data-ttu-id="bff3e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bff3e-117">-DefaultProfile</span></span>
<span data-ttu-id="bff3e-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bff3e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bff3e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="bff3e-119">-Force</span></span>
<span data-ttu-id="bff3e-120">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="bff3e-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="bff3e-121">-Local</span><span class="sxs-lookup"><span data-stu-id="bff3e-121">-Location</span></span>
<span data-ttu-id="bff3e-122">ponto.</span><span class="sxs-lookup"><span data-stu-id="bff3e-122">location.</span></span>

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

### <span data-ttu-id="bff3e-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="bff3e-123">-Name</span></span>
<span data-ttu-id="bff3e-124">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="bff3e-124">The resource name.</span></span>

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

### <span data-ttu-id="bff3e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bff3e-125">-ResourceGroupName</span></span>
<span data-ttu-id="bff3e-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bff3e-126">The resource group name.</span></span>

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

### <span data-ttu-id="bff3e-127">-Marca</span><span class="sxs-lookup"><span data-stu-id="bff3e-127">-Tag</span></span>
<span data-ttu-id="bff3e-128">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="bff3e-128">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="bff3e-129">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="bff3e-129">-ThreatIntelMode</span></span>
<span data-ttu-id="bff3e-130">O modo de operação para inteligência de ameaças.</span><span class="sxs-lookup"><span data-stu-id="bff3e-130">The operation mode for Threat Intelligence.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bff3e-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bff3e-131">-Confirm</span></span>
<span data-ttu-id="bff3e-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bff3e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bff3e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bff3e-133">-WhatIf</span></span>
<span data-ttu-id="bff3e-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bff3e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bff3e-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bff3e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bff3e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bff3e-136">CommonParameters</span></span>
<span data-ttu-id="bff3e-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bff3e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bff3e-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bff3e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bff3e-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bff3e-139">INPUTS</span></span>

### <span data-ttu-id="bff3e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="bff3e-140">System.String</span></span>

### <span data-ttu-id="bff3e-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bff3e-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bff3e-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bff3e-142">OUTPUTS</span></span>

### <span data-ttu-id="bff3e-143">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="bff3e-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="bff3e-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bff3e-144">NOTES</span></span>

## <span data-ttu-id="bff3e-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bff3e-145">RELATED LINKS</span></span>
