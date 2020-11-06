---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMConfig.md
ms.openlocfilehash: 2022a8a830d868f412e505f23e65c4c297bea543
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441167"
---
# <span data-ttu-id="e7fc2-101">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="e7fc2-101">New-AzureRmVMConfig</span></span>

## <span data-ttu-id="e7fc2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e7fc2-102">SYNOPSIS</span></span>
<span data-ttu-id="e7fc2-103">Cria um objeto de máquina virtual configurável.</span><span class="sxs-lookup"><span data-stu-id="e7fc2-103">Creates a configurable virtual machine object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7fc2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e7fc2-104">SYNTAX</span></span>

```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [[-IdentityType] <ResourceIdentityType>] [-AssignIdentity] [-Zone <String[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7fc2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e7fc2-105">DESCRIPTION</span></span>
<span data-ttu-id="e7fc2-106">O cmdlet **New-AzureRmVMConfig** cria um objeto de máquina virtual local configurável para o Azure.</span><span class="sxs-lookup"><span data-stu-id="e7fc2-106">The **New-AzureRmVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="e7fc2-107">Outros cmdlets podem ser usados para configurar um objeto de máquina virtual, como Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface e Set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="e7fc2-107">Other cmdlets can be used to configure a virtual machine object, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

## <span data-ttu-id="e7fc2-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e7fc2-108">EXAMPLES</span></span>

### <span data-ttu-id="e7fc2-109">Exemplo 1: criar um objeto de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="e7fc2-109">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="e7fc2-110">O primeiro comando obtém o conjunto de disponibilidade chamado AvailablitySet03 no grupo de recursos chamado ResourceGroup11 e, em seguida, armazena esse objeto na variável $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="e7fc2-110">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="e7fc2-111">O segundo comando cria um objeto de máquina virtual e, em seguida, armazena-o na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e7fc2-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="e7fc2-112">O comando atribui um nome e um tamanho para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e7fc2-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="e7fc2-113">A máquina virtual pertence ao conjunto de disponibilidade armazenado em $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="e7fc2-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="e7fc2-114">OS</span><span class="sxs-lookup"><span data-stu-id="e7fc2-114">PARAMETERS</span></span>

### <span data-ttu-id="e7fc2-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="e7fc2-115">-AssignIdentity</span></span>
<span data-ttu-id="e7fc2-116">Especifique a identidade atribuída ao sistema para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e7fc2-116">Specify the system assigned identity for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7fc2-117">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="e7fc2-117">-AvailabilitySetId</span></span>
<span data-ttu-id="e7fc2-118">Especifica a ID de um conjunto de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="e7fc2-118">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="e7fc2-119">Para obter um objeto do conjunto de disponibilidade, use o cmdlet Get-AzureRmAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="e7fc2-119">To obtain an availability set object, use the Get-AzureRmAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="e7fc2-120">O objeto de conjunto de disponibilidade contém uma propriedade de ID.</span><span class="sxs-lookup"><span data-stu-id="e7fc2-120">The availability set object contains an ID property.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7fc2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7fc2-121">-DefaultProfile</span></span>
<span data-ttu-id="e7fc2-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e7fc2-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7fc2-123">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="e7fc2-123">-IdentityType</span></span>
<span data-ttu-id="e7fc2-124">A identidade da máquina virtual, se estiver configurada.</span><span class="sxs-lookup"><span data-stu-id="e7fc2-124">The identity of the virtual machine, if configured.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: (All)
Aliases: 
Accepted values: SystemAssigned

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7fc2-125">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="e7fc2-125">-LicenseType</span></span>
<span data-ttu-id="e7fc2-126">O tipo de licença, que é para colocar seu próprio cenário de licença.</span><span class="sxs-lookup"><span data-stu-id="e7fc2-126">The license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7fc2-127">-Marcas</span><span class="sxs-lookup"><span data-stu-id="e7fc2-127">-Tags</span></span>
<span data-ttu-id="e7fc2-128">As marcas anexadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="e7fc2-128">The tags attached to the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7fc2-129">-VMName</span><span class="sxs-lookup"><span data-stu-id="e7fc2-129">-VMName</span></span>
<span data-ttu-id="e7fc2-130">Especifica um nome para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e7fc2-130">Specifies a name for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7fc2-131">-VMSize</span><span class="sxs-lookup"><span data-stu-id="e7fc2-131">-VMSize</span></span>
<span data-ttu-id="e7fc2-132">Especifica o tamanho da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e7fc2-132">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="e7fc2-133">-Zone</span><span class="sxs-lookup"><span data-stu-id="e7fc2-133">-Zone</span></span>
<span data-ttu-id="e7fc2-134">Especifica a lista de zonas para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e7fc2-134">Specifies the zone list for the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7fc2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7fc2-135">CommonParameters</span></span>
<span data-ttu-id="e7fc2-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7fc2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7fc2-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7fc2-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7fc2-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e7fc2-138">INPUTS</span></span>

## <span data-ttu-id="e7fc2-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e7fc2-139">OUTPUTS</span></span>

## <span data-ttu-id="e7fc2-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e7fc2-140">NOTES</span></span>

## <span data-ttu-id="e7fc2-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e7fc2-141">RELATED LINKS</span></span>

[<span data-ttu-id="e7fc2-142">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e7fc2-142">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="e7fc2-143">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="e7fc2-143">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="e7fc2-144">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="e7fc2-144">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="e7fc2-145">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e7fc2-145">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)


