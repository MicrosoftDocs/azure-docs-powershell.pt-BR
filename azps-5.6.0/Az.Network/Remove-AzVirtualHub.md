---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
ms.openlocfilehash: 7a5724346f1b94af0dbc07df16f9cdab5f798523
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892416"
---
# <span data-ttu-id="17230-101">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="17230-101">Remove-AzVirtualHub</span></span>

## <span data-ttu-id="17230-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17230-102">SYNOPSIS</span></span>
<span data-ttu-id="17230-103">Remove um recurso do Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="17230-103">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="17230-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="17230-104">SYNTAX</span></span>

### <span data-ttu-id="17230-105">ByVirtualHubName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="17230-105">ByVirtualHubName (Default)</span></span>
```
Remove-AzVirtualHub -ResourceGroupName <String> -Name <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17230-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="17230-106">ByVirtualHubResourceId</span></span>
```
Remove-AzVirtualHub -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17230-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="17230-107">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHub -InputObject <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17230-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="17230-108">DESCRIPTION</span></span>
<span data-ttu-id="17230-109">Remove um recurso do Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="17230-109">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="17230-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="17230-110">EXAMPLES</span></span>

### <span data-ttu-id="17230-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="17230-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="17230-112">O acima criará um grupo de recursos "testRG", uma WAN Virtual e um Hub Virtual no Oeste dos EUA nesse grupo de recursos no Azure.</span><span class="sxs-lookup"><span data-stu-id="17230-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="17230-113">O hub virtual terá o espaço de endereço "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="17230-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="17230-114">Em seguida, exclui o hub virtual usando resourceGroupName e ResourceName.</span><span class="sxs-lookup"><span data-stu-id="17230-114">It then deletes the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="17230-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="17230-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -InputObject $virtualHub
```

<span data-ttu-id="17230-116">O acima criará um grupo de recursos "testRG", uma WAN Virtual e um Hub Virtual no Oeste dos EUA nesse grupo de recursos no Azure.</span><span class="sxs-lookup"><span data-stu-id="17230-116">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="17230-117">O hub virtual terá o espaço de endereço "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="17230-117">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="17230-118">Em seguida, exclui o hub virtual usando um objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="17230-118">It then deletes the virtual hub using an input object.</span></span> <span data-ttu-id="17230-119">O objeto de entrada é do tipo PSVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="17230-119">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="17230-120">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="17230-120">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Remove-AzVirtualHub
```

<span data-ttu-id="17230-121">O acima criará um grupo de recursos "testRG", uma WAN Virtual e um Hub Virtual no Oeste dos EUA nesse grupo de recursos no Azure.</span><span class="sxs-lookup"><span data-stu-id="17230-121">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="17230-122">O hub virtual terá o espaço de endereço "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="17230-122">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="17230-123">Em seguida, exclui o hub virtual usando a canalização do powershell usando a saída de Get-AzVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="17230-123">It then deletes the virtual hub using powershell piping using output from Get-AzVirtualHub.</span></span>

## <span data-ttu-id="17230-124">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="17230-124">PARAMETERS</span></span>

### <span data-ttu-id="17230-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="17230-125">-AsJob</span></span>
<span data-ttu-id="17230-126">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="17230-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="17230-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17230-127">-DefaultProfile</span></span>
<span data-ttu-id="17230-128">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="17230-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17230-129">-Force</span><span class="sxs-lookup"><span data-stu-id="17230-129">-Force</span></span>
<span data-ttu-id="17230-130">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="17230-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="17230-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17230-131">-InputObject</span></span>
<span data-ttu-id="17230-132">O objeto de hub virtual a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="17230-132">The Virtual hub object to be modified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17230-133">-Name</span><span class="sxs-lookup"><span data-stu-id="17230-133">-Name</span></span>
<span data-ttu-id="17230-134">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="17230-134">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17230-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="17230-135">-PassThru</span></span>
<span data-ttu-id="17230-136">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="17230-136">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="17230-137">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="17230-137">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="17230-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17230-138">-ResourceGroupName</span></span>
<span data-ttu-id="17230-139">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="17230-139">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17230-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17230-140">-ResourceId</span></span>
<span data-ttu-id="17230-141">A id de recurso do hub virtual a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="17230-141">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17230-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17230-142">-Confirm</span></span>
<span data-ttu-id="17230-143">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17230-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17230-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17230-144">-WhatIf</span></span>
<span data-ttu-id="17230-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="17230-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17230-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="17230-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17230-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17230-147">CommonParameters</span></span>
<span data-ttu-id="17230-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17230-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17230-149">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17230-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17230-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="17230-150">INPUTS</span></span>

### <span data-ttu-id="17230-151">System.String</span><span class="sxs-lookup"><span data-stu-id="17230-151">System.String</span></span>

### <span data-ttu-id="17230-152">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="17230-152">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="17230-153">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="17230-153">OUTPUTS</span></span>

### <span data-ttu-id="17230-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="17230-154">System.Boolean</span></span>

## <span data-ttu-id="17230-155">NOTES</span><span class="sxs-lookup"><span data-stu-id="17230-155">NOTES</span></span>

## <span data-ttu-id="17230-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="17230-156">RELATED LINKS</span></span>

[<span data-ttu-id="17230-157">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="17230-157">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="17230-158">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="17230-158">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="17230-159">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="17230-159">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
