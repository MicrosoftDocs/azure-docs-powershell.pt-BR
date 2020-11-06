---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualHub.md
ms.openlocfilehash: 65d319749424697c882012d23bf12f87f92adbc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440332"
---
# <span data-ttu-id="9df3d-101">Remove-AzureRmVirtualHub</span><span class="sxs-lookup"><span data-stu-id="9df3d-101">Remove-AzureRmVirtualHub</span></span>

## <span data-ttu-id="9df3d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9df3d-102">SYNOPSIS</span></span>
<span data-ttu-id="9df3d-103">Remove um recurso do VirtualHub do Azure.</span><span class="sxs-lookup"><span data-stu-id="9df3d-103">Removes an Azure VirtualHub resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9df3d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9df3d-104">SYNTAX</span></span>

### <span data-ttu-id="9df3d-105">ByVirtualHubName (padrão)</span><span class="sxs-lookup"><span data-stu-id="9df3d-105">ByVirtualHubName (Default)</span></span>
```
Remove-AzureRmVirtualHub -ResourceGroupName <String> -Name <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9df3d-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="9df3d-106">ByVirtualHubResourceId</span></span>
```
Remove-AzureRmVirtualHub -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9df3d-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="9df3d-107">ByVirtualHubObject</span></span>
```
Remove-AzureRmVirtualHub -InputObject <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9df3d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9df3d-108">DESCRIPTION</span></span>
<span data-ttu-id="9df3d-109">Remove um recurso do VirtualHub do Azure.</span><span class="sxs-lookup"><span data-stu-id="9df3d-109">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="9df3d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9df3d-110">EXAMPLES</span></span>

### <span data-ttu-id="9df3d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9df3d-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzureRmVirtualHub -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="9df3d-112">A seguir, você criará um grupo de recursos "testRG", uma WAN virtual e um hub virtual no oeste dos EUA no grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="9df3d-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="9df3d-113">O Hub virtual terá o espaço de endereço "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="9df3d-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="9df3d-114">Em seguida, ele exclui o Hub virtual usando seu ResourceGroupName e ResourceManager.</span><span class="sxs-lookup"><span data-stu-id="9df3d-114">It then deletes the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="9df3d-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9df3d-115">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzureRmVirtualHub -InputObject $virtualHub
```

<span data-ttu-id="9df3d-116">A seguir, você criará um grupo de recursos "testRG", uma WAN virtual e um hub virtual no oeste dos EUA no grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="9df3d-116">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="9df3d-117">O Hub virtual terá o espaço de endereço "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="9df3d-117">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="9df3d-118">Em seguida, ele exclui o Hub virtual usando um objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="9df3d-118">It then deletes the virtual hub using an input object.</span></span> <span data-ttu-id="9df3d-119">O objeto de entrada é do tipo PSVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="9df3d-119">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="9df3d-120">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="9df3d-120">Example 3</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzureRmVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Remove-AzureRmVirtualHub
```

<span data-ttu-id="9df3d-121">A seguir, você criará um grupo de recursos "testRG", uma WAN virtual e um hub virtual no oeste dos EUA no grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="9df3d-121">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="9df3d-122">O Hub virtual terá o espaço de endereço "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="9df3d-122">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="9df3d-123">Em seguida, ele exclui o Hub virtual que usa o pipe do PowerShell usando a saída do Get-AzureRmVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="9df3d-123">It then deletes the virtual hub using powershell piping using output from Get-AzureRmVirtualHub.</span></span>

## <span data-ttu-id="9df3d-124">OS</span><span class="sxs-lookup"><span data-stu-id="9df3d-124">PARAMETERS</span></span>

### <span data-ttu-id="9df3d-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9df3d-125">-AsJob</span></span>
<span data-ttu-id="9df3d-126">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9df3d-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9df3d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9df3d-127">-DefaultProfile</span></span>
<span data-ttu-id="9df3d-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9df3d-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9df3d-129">-Force</span><span class="sxs-lookup"><span data-stu-id="9df3d-129">-Force</span></span>
<span data-ttu-id="9df3d-130">Não pedir confirmação se quiser sobreformular um recurso</span><span class="sxs-lookup"><span data-stu-id="9df3d-130">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="9df3d-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9df3d-131">-InputObject</span></span>
<span data-ttu-id="9df3d-132">O objeto de Hub virtual a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="9df3d-132">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="9df3d-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="9df3d-133">-Name</span></span>
<span data-ttu-id="9df3d-134">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="9df3d-134">The resource name.</span></span>

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

### <span data-ttu-id="9df3d-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9df3d-135">-PassThru</span></span>
<span data-ttu-id="9df3d-136">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="9df3d-136">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9df3d-137">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="9df3d-137">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9df3d-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9df3d-138">-ResourceGroupName</span></span>
<span data-ttu-id="9df3d-139">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9df3d-139">The resource group name.</span></span>

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

### <span data-ttu-id="9df3d-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9df3d-140">-ResourceId</span></span>
<span data-ttu-id="9df3d-141">A ID do recurso do Hub virtual a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="9df3d-141">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="9df3d-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9df3d-142">-Confirm</span></span>
<span data-ttu-id="9df3d-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9df3d-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9df3d-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9df3d-144">-WhatIf</span></span>
<span data-ttu-id="9df3d-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9df3d-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9df3d-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9df3d-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9df3d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9df3d-147">CommonParameters</span></span>
<span data-ttu-id="9df3d-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9df3d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9df3d-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9df3d-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9df3d-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9df3d-150">INPUTS</span></span>

### <span data-ttu-id="9df3d-151">System. String</span><span class="sxs-lookup"><span data-stu-id="9df3d-151">System.String</span></span>

### <span data-ttu-id="9df3d-152">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="9df3d-152">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="9df3d-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9df3d-153">OUTPUTS</span></span>

### <span data-ttu-id="9df3d-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9df3d-154">System.Boolean</span></span>

## <span data-ttu-id="9df3d-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9df3d-155">NOTES</span></span>

## <span data-ttu-id="9df3d-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9df3d-156">RELATED LINKS</span></span>
