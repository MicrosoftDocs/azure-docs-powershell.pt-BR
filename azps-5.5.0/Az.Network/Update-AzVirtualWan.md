---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
ms.openlocfilehash: e93bcc320f14a8311a29c6be9824da16506ea499
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118244"
---
# <span data-ttu-id="facd3-101">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="facd3-101">Update-AzVirtualWan</span></span>

## <span data-ttu-id="facd3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="facd3-102">SYNOPSIS</span></span>
<span data-ttu-id="facd3-103">Atualiza uma WAN virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="facd3-103">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="facd3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="facd3-104">SYNTAX</span></span>

### <span data-ttu-id="facd3-105">ByVirtualWanName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="facd3-105">ByVirtualWanName (Default)</span></span>
```
Update-AzVirtualWan -ResourceGroupName <String> -Name <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="facd3-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="facd3-106">ByVirtualWanObject</span></span>
```
Update-AzVirtualWan -InputObject <PSVirtualWan> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="facd3-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="facd3-107">ByVirtualWanResourceId</span></span>
```
Update-AzVirtualWan -ResourceId <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="facd3-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="facd3-108">DESCRIPTION</span></span>
<span data-ttu-id="facd3-109">Atualiza uma WAN virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="facd3-109">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="facd3-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="facd3-110">EXAMPLES</span></span>

### <span data-ttu-id="facd3-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="facd3-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> Update-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -AllowBranchToBranchTraffic $true -AllowVnetToVnetTraffic $false

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
VirtualWANType             : Standard
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="facd3-112">O exemplo acima criará um grupo de recursos "testRG" na região "Oeste dos EUA" e uma WAN Virtual do Azure nesse grupo de recursos no Azure.</span><span class="sxs-lookup"><span data-stu-id="facd3-112">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN in that resource group in Azure.</span></span> <span data-ttu-id="facd3-113">O VirtualWan é atualizado com novas propriedades.</span><span class="sxs-lookup"><span data-stu-id="facd3-113">VirtualWan is updated with new properties.</span></span>

## <span data-ttu-id="facd3-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="facd3-114">PARAMETERS</span></span>

### <span data-ttu-id="facd3-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="facd3-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="facd3-116">Permitir a ramificação para o tráfego de VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="facd3-116">Allow branch to branch traffic for VirtualWan.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="facd3-117">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="facd3-117">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="facd3-118">Permitir o tráfego vnet para vnet para VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="facd3-118">Allow vnet to vnet traffic for VirtualWan.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="facd3-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="facd3-119">-AsJob</span></span>
<span data-ttu-id="facd3-120">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="facd3-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="facd3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="facd3-121">-DefaultProfile</span></span>
<span data-ttu-id="facd3-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="facd3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="facd3-123">-Forçar</span><span class="sxs-lookup"><span data-stu-id="facd3-123">-Force</span></span>
<span data-ttu-id="facd3-124">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="facd3-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="facd3-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="facd3-125">-InputObject</span></span>
<span data-ttu-id="facd3-126">O objeto wan virtual a ser modificado</span><span class="sxs-lookup"><span data-stu-id="facd3-126">The virtual wan object to be modified</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="facd3-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="facd3-127">-Name</span></span>
<span data-ttu-id="facd3-128">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="facd3-128">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="facd3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="facd3-129">-ResourceGroupName</span></span>
<span data-ttu-id="facd3-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="facd3-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="facd3-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="facd3-131">-ResourceId</span></span>
<span data-ttu-id="facd3-132">A ID de recurso do Azure para a wan virtual.</span><span class="sxs-lookup"><span data-stu-id="facd3-132">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="facd3-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="facd3-133">-Tag</span></span>
<span data-ttu-id="facd3-134">Uma tabela hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="facd3-134">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="facd3-135">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="facd3-135">-VirtualWANType</span></span>
<span data-ttu-id="facd3-136">O tipo de Wan Virtual.</span><span class="sxs-lookup"><span data-stu-id="facd3-136">The type of the Virtual Wan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="facd3-137">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="facd3-137">-Confirm</span></span>
<span data-ttu-id="facd3-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="facd3-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="facd3-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="facd3-139">-WhatIf</span></span>
<span data-ttu-id="facd3-140">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="facd3-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="facd3-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="facd3-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="facd3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="facd3-142">CommonParameters</span></span>
<span data-ttu-id="facd3-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="facd3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="facd3-144">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="facd3-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="facd3-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="facd3-145">INPUTS</span></span>

### <span data-ttu-id="facd3-146">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="facd3-146">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="facd3-147">System.String</span><span class="sxs-lookup"><span data-stu-id="facd3-147">System.String</span></span>

## <span data-ttu-id="facd3-148">Saídas</span><span class="sxs-lookup"><span data-stu-id="facd3-148">OUTPUTS</span></span>

### <span data-ttu-id="facd3-149">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="facd3-149">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="facd3-150">Notas</span><span class="sxs-lookup"><span data-stu-id="facd3-150">NOTES</span></span>

## <span data-ttu-id="facd3-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="facd3-151">RELATED LINKS</span></span>

[<span data-ttu-id="facd3-152">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="facd3-152">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="facd3-153">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="facd3-153">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="facd3-154">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="facd3-154">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)
