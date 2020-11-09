---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualApplianceSite.md
ms.openlocfilehash: 4d63726f67cb43f34e58c8e560a08adefce5fcbd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284051"
---
# <span data-ttu-id="93dd2-101">Update-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="93dd2-101">Update-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="93dd2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="93dd2-102">SYNOPSIS</span></span>
<span data-ttu-id="93dd2-103">Alterar ou modificar um site de dispositivo virtual conectado a um recurso de dispositivo virtual de rede.</span><span class="sxs-lookup"><span data-stu-id="93dd2-103">Change or Modify a Virtual Appliance site connected to a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="93dd2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93dd2-104">SYNTAX</span></span>

```
Update-AzVirtualApplianceSite -Name <String> -ResourceGroupName <String> -NetworkVirtualApplianceId <String>
 [-AddresssPrefix <String>] [-O365Policy <PSOffice365PolicyProperties>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93dd2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="93dd2-105">DESCRIPTION</span></span>
<span data-ttu-id="93dd2-106">O comando Update-AzVirtualApplianceSite modifica um recurso de site de dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="93dd2-106">The Update-AzVirtualApplianceSite command modifies a Virtual Appliance site resource.</span></span>

## <span data-ttu-id="93dd2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="93dd2-107">EXAMPLES</span></span>

### <span data-ttu-id="93dd2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="93dd2-108">Example 1</span></span>
```powershell
PS C:\> $nva=Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
PS C:\> Update-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -AddresssPrefix 10.0.4.0/24 -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="93dd2-109">Modifique o prefixo do endereço de um recurso de site do Virtual Appliance.</span><span class="sxs-lookup"><span data-stu-id="93dd2-109">Modify the address prefix for a Virtual Appliance site resource.</span></span>

## <span data-ttu-id="93dd2-110">OS</span><span class="sxs-lookup"><span data-stu-id="93dd2-110">PARAMETERS</span></span>

### <span data-ttu-id="93dd2-111">-AddresssPrefix</span><span class="sxs-lookup"><span data-stu-id="93dd2-111">-AddresssPrefix</span></span>
<span data-ttu-id="93dd2-112">O prefixo do endereço do site.</span><span class="sxs-lookup"><span data-stu-id="93dd2-112">The address prefix for the site.</span></span>

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

### <span data-ttu-id="93dd2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="93dd2-113">-AsJob</span></span>
<span data-ttu-id="93dd2-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="93dd2-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="93dd2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93dd2-115">-DefaultProfile</span></span>
<span data-ttu-id="93dd2-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="93dd2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93dd2-117">-Force</span><span class="sxs-lookup"><span data-stu-id="93dd2-117">-Force</span></span>
<span data-ttu-id="93dd2-118">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="93dd2-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="93dd2-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="93dd2-119">-Name</span></span>
<span data-ttu-id="93dd2-120">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="93dd2-120">The resource name.</span></span>

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

### <span data-ttu-id="93dd2-121">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="93dd2-121">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="93dd2-122">Dispositivo virtual de rede ao qual este site está associado.</span><span class="sxs-lookup"><span data-stu-id="93dd2-122">Network virtual appliance that this site is attached to.</span></span>

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

### <span data-ttu-id="93dd2-123">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="93dd2-123">-O365Policy</span></span>
<span data-ttu-id="93dd2-124">Política de debates do Office 365.</span><span class="sxs-lookup"><span data-stu-id="93dd2-124">Office 365 breakout policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93dd2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93dd2-125">-ResourceGroupName</span></span>
<span data-ttu-id="93dd2-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="93dd2-126">The resource group name.</span></span>

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

### <span data-ttu-id="93dd2-127">-Marca</span><span class="sxs-lookup"><span data-stu-id="93dd2-127">-Tag</span></span>
<span data-ttu-id="93dd2-128">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="93dd2-128">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="93dd2-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="93dd2-129">-Confirm</span></span>
<span data-ttu-id="93dd2-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93dd2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93dd2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93dd2-131">-WhatIf</span></span>
<span data-ttu-id="93dd2-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="93dd2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93dd2-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="93dd2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93dd2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93dd2-134">CommonParameters</span></span>
<span data-ttu-id="93dd2-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93dd2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93dd2-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93dd2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93dd2-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="93dd2-137">INPUTS</span></span>

### <span data-ttu-id="93dd2-138">System. String</span><span class="sxs-lookup"><span data-stu-id="93dd2-138">System.String</span></span>

### <span data-ttu-id="93dd2-139">Microsoft. Azure. Commands. Network. Models. PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="93dd2-139">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

### <span data-ttu-id="93dd2-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="93dd2-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="93dd2-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="93dd2-141">OUTPUTS</span></span>

### <span data-ttu-id="93dd2-142">Microsoft. Azure. Commands. Network. Models. PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="93dd2-142">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="93dd2-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="93dd2-143">NOTES</span></span>

## <span data-ttu-id="93dd2-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="93dd2-144">RELATED LINKS</span></span>
