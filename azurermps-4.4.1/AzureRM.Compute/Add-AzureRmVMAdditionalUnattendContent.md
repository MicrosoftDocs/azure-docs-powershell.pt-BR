---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMAdditionalUnattendContent.md
ms.openlocfilehash: 66b3f8da0f133bf4f5c173d1cf7dbb03d8dc7795
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439964"
---
# <span data-ttu-id="aa0cc-101">Add-AzureRmVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="aa0cc-101">Add-AzureRmVMAdditionalUnattendContent</span></span>

## <span data-ttu-id="aa0cc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aa0cc-102">SYNOPSIS</span></span>
<span data-ttu-id="aa0cc-103">Adiciona informações ao arquivo de resposta da instalação autônoma do Windows.</span><span class="sxs-lookup"><span data-stu-id="aa0cc-103">Adds information to the unattended Windows Setup answer file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa0cc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aa0cc-104">SYNTAX</span></span>

```
Add-AzureRmVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa0cc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aa0cc-105">DESCRIPTION</span></span>
<span data-ttu-id="aa0cc-106">O cmdlet **Add-AzureRmVMAdditionalUnattendContent** adiciona informações ao arquivo de resposta da instalação autônoma do Windows.</span><span class="sxs-lookup"><span data-stu-id="aa0cc-106">The **Add-AzureRmVMAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>
<span data-ttu-id="aa0cc-107">Especifique as informações formatadas. XML adicionais de base 64 codificadas que esse cmdlet adiciona ao arquivo unattend.xml.</span><span class="sxs-lookup"><span data-stu-id="aa0cc-107">Specify additional base 64 encoded .xml formatted information that this cmdlet adds to the unattend.xml file.</span></span>

## <span data-ttu-id="aa0cc-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aa0cc-108">EXAMPLES</span></span>

### <span data-ttu-id="aa0cc-109">Exemplo 1: adicionar conteúdo a unattend.xml</span><span class="sxs-lookup"><span data-stu-id="aa0cc-109">Example 1: Add content to unattend.xml</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzureRmVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

<span data-ttu-id="aa0cc-110">O primeiro comando obtém o conjunto de disponibilidade chamado AvailablitySet03 no grupo de recursos chamado ResourceGroup11 e, em seguida, armazena esse objeto na variável $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="aa0cc-110">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="aa0cc-111">O segundo comando cria um objeto de máquina virtual e, em seguida, armazena-o na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="aa0cc-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="aa0cc-112">O comando atribui um nome e um tamanho para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="aa0cc-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="aa0cc-113">A máquina virtual pertence ao conjunto de disponibilidade armazenado em $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="aa0cc-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="aa0cc-114">O terceiro comando cria um objeto Credential usando o cmdlet Get-Credential e armazena o resultado na variável $Credential.</span><span class="sxs-lookup"><span data-stu-id="aa0cc-114">The third command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="aa0cc-115">O comando solicita um nome de usuário e uma senha.</span><span class="sxs-lookup"><span data-stu-id="aa0cc-115">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="aa0cc-116">Para obter mais informações, digite `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="aa0cc-116">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="aa0cc-117">O quarto comando usa o cmdlet **set-AzureRmVMOperatingSystem** para configurar a máquina virtual armazenada em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="aa0cc-117">The fourth command uses the **Set-AzureRmVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="aa0cc-118">O quinto comando atribui conteúdo à variável $AucContent.</span><span class="sxs-lookup"><span data-stu-id="aa0cc-118">The fifth command assigns content to the $AucContent variable.</span></span>
<span data-ttu-id="aa0cc-119">O conteúdo inclui uma senha.</span><span class="sxs-lookup"><span data-stu-id="aa0cc-119">The content includes a password.</span></span>

<span data-ttu-id="aa0cc-120">O comando final adiciona o conteúdo armazenado em $AucContent ao arquivo unattend.xml.</span><span class="sxs-lookup"><span data-stu-id="aa0cc-120">The final command adds the content stored in $AucContent to the unattend.xml file.</span></span>

## <span data-ttu-id="aa0cc-121">OS</span><span class="sxs-lookup"><span data-stu-id="aa0cc-121">PARAMETERS</span></span>

### <span data-ttu-id="aa0cc-122">-Conteúdo</span><span class="sxs-lookup"><span data-stu-id="aa0cc-122">-Content</span></span>
<span data-ttu-id="aa0cc-123">Especifica conteúdo formatado XML em base 64.</span><span class="sxs-lookup"><span data-stu-id="aa0cc-123">Specifies base 64 encoded XML formatted content.</span></span>
<span data-ttu-id="aa0cc-124">Esse cmdlet adiciona o conteúdo ao arquivo unattend.xml.</span><span class="sxs-lookup"><span data-stu-id="aa0cc-124">This cmdlet adds the content to the unattend.xml file.</span></span>
<span data-ttu-id="aa0cc-125">O conteúdo XML deve ter menos de 4 KB e deve incluir o elemento raiz para a configuração ou o recurso que esse cmdlet insere.</span><span class="sxs-lookup"><span data-stu-id="aa0cc-125">The XML content must be less than 4 KB and must include the root element for the setting or feature that this cmdlet inserts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa0cc-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa0cc-126">-DefaultProfile</span></span>
<span data-ttu-id="aa0cc-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aa0cc-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa0cc-128">-SettingName</span><span class="sxs-lookup"><span data-stu-id="aa0cc-128">-SettingName</span></span>
<span data-ttu-id="aa0cc-129">Especifica o nome da configuração à qual o conteúdo se aplica.</span><span class="sxs-lookup"><span data-stu-id="aa0cc-129">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="aa0cc-130">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="aa0cc-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aa0cc-131">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="aa0cc-131">FirstLogonCommands</span></span>
- <span data-ttu-id="aa0cc-132">Logon automático</span><span class="sxs-lookup"><span data-stu-id="aa0cc-132">AutoLogon</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.SettingNames]
Parameter Sets: (All)
Aliases: 
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa0cc-133">-VM</span><span class="sxs-lookup"><span data-stu-id="aa0cc-133">-VM</span></span>
<span data-ttu-id="aa0cc-134">Especifica o objeto da máquina virtual que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="aa0cc-134">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="aa0cc-135">Para obter um objeto de máquina virtual, use o cmdlet [Get-AzureRmVM](./Get-AzureRmVM.md) .</span><span class="sxs-lookup"><span data-stu-id="aa0cc-135">To obtain a virtual machine object, use the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="aa0cc-136">Crie um objeto de máquina virtual usando o cmdlet [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="aa0cc-136">Create a virtual machine object by using the [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa0cc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa0cc-137">CommonParameters</span></span>
<span data-ttu-id="aa0cc-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa0cc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa0cc-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa0cc-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa0cc-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aa0cc-140">INPUTS</span></span>

## <span data-ttu-id="aa0cc-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aa0cc-141">OUTPUTS</span></span>

## <span data-ttu-id="aa0cc-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aa0cc-142">NOTES</span></span>

## <span data-ttu-id="aa0cc-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aa0cc-143">RELATED LINKS</span></span>

[<span data-ttu-id="aa0cc-144">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="aa0cc-144">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="aa0cc-145">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="aa0cc-145">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="aa0cc-146">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="aa0cc-146">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
