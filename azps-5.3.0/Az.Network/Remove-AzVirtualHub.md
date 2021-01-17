---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
ms.openlocfilehash: 116cffabc942572db48d6f86b469a954bccbc1c2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434679"
---
# <span data-ttu-id="ea0c2-101">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="ea0c2-101">Remove-AzVirtualHub</span></span>

## <span data-ttu-id="ea0c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ea0c2-102">SYNOPSIS</span></span>
<span data-ttu-id="ea0c2-103">Remove um recurso do VirtualHub do Azure.</span><span class="sxs-lookup"><span data-stu-id="ea0c2-103">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="ea0c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea0c2-104">SYNTAX</span></span>

### <span data-ttu-id="ea0c2-105">ByVirtualHubName (padrão)</span><span class="sxs-lookup"><span data-stu-id="ea0c2-105">ByVirtualHubName (Default)</span></span>
```
Remove-AzVirtualHub -ResourceGroupName <String> -Name <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea0c2-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="ea0c2-106">ByVirtualHubResourceId</span></span>
```
Remove-AzVirtualHub -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea0c2-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="ea0c2-107">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHub -InputObject <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea0c2-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ea0c2-108">DESCRIPTION</span></span>
<span data-ttu-id="ea0c2-109">Remove um recurso do VirtualHub do Azure.</span><span class="sxs-lookup"><span data-stu-id="ea0c2-109">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="ea0c2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ea0c2-110">EXAMPLES</span></span>

### <span data-ttu-id="ea0c2-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ea0c2-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="ea0c2-112">A seguir, você criará um grupo de recursos "testRG", uma WAN virtual e um hub virtual no oeste dos EUA no grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="ea0c2-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="ea0c2-113">O Hub virtual terá o espaço de endereço "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="ea0c2-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="ea0c2-114">Em seguida, ele exclui o Hub virtual usando seu ResourceGroupName e ResourceManager.</span><span class="sxs-lookup"><span data-stu-id="ea0c2-114">It then deletes the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="ea0c2-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ea0c2-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -InputObject $virtualHub
```

<span data-ttu-id="ea0c2-116">A seguir, você criará um grupo de recursos "testRG", uma WAN virtual e um hub virtual no oeste dos EUA no grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="ea0c2-116">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="ea0c2-117">O Hub virtual terá o espaço de endereço "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="ea0c2-117">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="ea0c2-118">Em seguida, ele exclui o Hub virtual usando um objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="ea0c2-118">It then deletes the virtual hub using an input object.</span></span> <span data-ttu-id="ea0c2-119">O objeto de entrada é do tipo PSVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="ea0c2-119">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="ea0c2-120">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="ea0c2-120">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Remove-AzVirtualHub
```

<span data-ttu-id="ea0c2-121">A seguir, você criará um grupo de recursos "testRG", uma WAN virtual e um hub virtual no oeste dos EUA no grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="ea0c2-121">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="ea0c2-122">O Hub virtual terá o espaço de endereço "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="ea0c2-122">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="ea0c2-123">Em seguida, ele exclui o Hub virtual que usa o pipe do PowerShell usando a saída do Get-AzVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="ea0c2-123">It then deletes the virtual hub using powershell piping using output from Get-AzVirtualHub.</span></span>

## <span data-ttu-id="ea0c2-124">OS</span><span class="sxs-lookup"><span data-stu-id="ea0c2-124">PARAMETERS</span></span>

### <span data-ttu-id="ea0c2-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea0c2-125">-AsJob</span></span>
<span data-ttu-id="ea0c2-126">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ea0c2-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ea0c2-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea0c2-127">-DefaultProfile</span></span>
<span data-ttu-id="ea0c2-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ea0c2-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea0c2-129">-Force</span><span class="sxs-lookup"><span data-stu-id="ea0c2-129">-Force</span></span>
<span data-ttu-id="ea0c2-130">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="ea0c2-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="ea0c2-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea0c2-131">-InputObject</span></span>
<span data-ttu-id="ea0c2-132">O objeto de Hub virtual a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="ea0c2-132">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="ea0c2-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="ea0c2-133">-Name</span></span>
<span data-ttu-id="ea0c2-134">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="ea0c2-134">The resource name.</span></span>

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

### <span data-ttu-id="ea0c2-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea0c2-135">-PassThru</span></span>
<span data-ttu-id="ea0c2-136">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="ea0c2-136">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ea0c2-137">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="ea0c2-137">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ea0c2-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea0c2-138">-ResourceGroupName</span></span>
<span data-ttu-id="ea0c2-139">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ea0c2-139">The resource group name.</span></span>

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

### <span data-ttu-id="ea0c2-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea0c2-140">-ResourceId</span></span>
<span data-ttu-id="ea0c2-141">A ID do recurso do Hub virtual a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="ea0c2-141">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="ea0c2-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ea0c2-142">-Confirm</span></span>
<span data-ttu-id="ea0c2-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea0c2-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea0c2-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea0c2-144">-WhatIf</span></span>
<span data-ttu-id="ea0c2-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ea0c2-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea0c2-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ea0c2-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea0c2-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea0c2-147">CommonParameters</span></span>
<span data-ttu-id="ea0c2-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea0c2-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea0c2-149">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea0c2-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea0c2-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ea0c2-150">INPUTS</span></span>

### <span data-ttu-id="ea0c2-151">System. String</span><span class="sxs-lookup"><span data-stu-id="ea0c2-151">System.String</span></span>

### <span data-ttu-id="ea0c2-152">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="ea0c2-152">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="ea0c2-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ea0c2-153">OUTPUTS</span></span>

### <span data-ttu-id="ea0c2-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ea0c2-154">System.Boolean</span></span>

## <span data-ttu-id="ea0c2-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ea0c2-155">NOTES</span></span>

## <span data-ttu-id="ea0c2-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ea0c2-156">RELATED LINKS</span></span>

[<span data-ttu-id="ea0c2-157">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="ea0c2-157">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="ea0c2-158">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="ea0c2-158">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="ea0c2-159">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="ea0c2-159">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
