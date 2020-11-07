---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
ms.openlocfilehash: e4359629da6f4df4c8da26e5ade2b2652c0762e4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775207"
---
# <span data-ttu-id="cc17d-101">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="cc17d-101">Add-AzVMAdditionalUnattendContent</span></span>

## <span data-ttu-id="cc17d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cc17d-102">SYNOPSIS</span></span>
<span data-ttu-id="cc17d-103">Adiciona informações ao arquivo de resposta da instalação autônoma do Windows.</span><span class="sxs-lookup"><span data-stu-id="cc17d-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="cc17d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cc17d-104">SYNTAX</span></span>

```
Add-AzVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc17d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cc17d-105">DESCRIPTION</span></span>
<span data-ttu-id="cc17d-106">O cmdlet **Add-AzVMAdditionalUnattendContent** adiciona informações ao arquivo de resposta da instalação autônoma do Windows.</span><span class="sxs-lookup"><span data-stu-id="cc17d-106">The **Add-AzVMAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>
<span data-ttu-id="cc17d-107">Especifique as informações formatadas. XML adicionais de base 64 codificadas que esse cmdlet adiciona ao arquivo unattend.xml.</span><span class="sxs-lookup"><span data-stu-id="cc17d-107">Specify additional base 64 encoded .xml formatted information that this cmdlet adds to the unattend.xml file.</span></span>

## <span data-ttu-id="cc17d-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cc17d-108">EXAMPLES</span></span>

### <span data-ttu-id="cc17d-109">Exemplo 1: adicionar conteúdo a unattend.xml</span><span class="sxs-lookup"><span data-stu-id="cc17d-109">Example 1: Add content to unattend.xml</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

<span data-ttu-id="cc17d-110">O primeiro comando obtém o conjunto de disponibilidade chamado AvailablitySet03 no grupo de recursos chamado ResourceGroup11 e, em seguida, armazena esse objeto na variável $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="cc17d-110">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="cc17d-111">O segundo comando cria um objeto de máquina virtual e, em seguida, armazena-o na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="cc17d-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="cc17d-112">O comando atribui um nome e um tamanho para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cc17d-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="cc17d-113">A máquina virtual pertence ao conjunto de disponibilidade armazenado em $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="cc17d-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="cc17d-114">O terceiro comando cria um objeto Credential usando o cmdlet Get-Credential e armazena o resultado na variável $Credential.</span><span class="sxs-lookup"><span data-stu-id="cc17d-114">The third command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="cc17d-115">O comando solicita um nome de usuário e uma senha.</span><span class="sxs-lookup"><span data-stu-id="cc17d-115">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="cc17d-116">Para obter mais informações, digite `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="cc17d-116">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="cc17d-117">O quarto comando usa o cmdlet **set-AzVMOperatingSystem** para configurar a máquina virtual armazenada em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="cc17d-117">The fourth command uses the **Set-AzVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="cc17d-118">O quinto comando atribui conteúdo à variável $AucContent.</span><span class="sxs-lookup"><span data-stu-id="cc17d-118">The fifth command assigns content to the $AucContent variable.</span></span>
<span data-ttu-id="cc17d-119">O conteúdo inclui uma senha.</span><span class="sxs-lookup"><span data-stu-id="cc17d-119">The content includes a password.</span></span>

<span data-ttu-id="cc17d-120">O comando final adiciona o conteúdo armazenado em $AucContent ao arquivo unattend.xml.</span><span class="sxs-lookup"><span data-stu-id="cc17d-120">The final command adds the content stored in $AucContent to the unattend.xml file.</span></span>

## <span data-ttu-id="cc17d-121">OS</span><span class="sxs-lookup"><span data-stu-id="cc17d-121">PARAMETERS</span></span>

### <span data-ttu-id="cc17d-122">-Conteúdo</span><span class="sxs-lookup"><span data-stu-id="cc17d-122">-Content</span></span>
<span data-ttu-id="cc17d-123">Especifica conteúdo formatado XML em base 64.</span><span class="sxs-lookup"><span data-stu-id="cc17d-123">Specifies base 64 encoded XML formatted content.</span></span>
<span data-ttu-id="cc17d-124">Esse cmdlet adiciona o conteúdo ao arquivo unattend.xml.</span><span class="sxs-lookup"><span data-stu-id="cc17d-124">This cmdlet adds the content to the unattend.xml file.</span></span>
<span data-ttu-id="cc17d-125">O conteúdo XML deve ter menos de 4 KB e deve incluir o elemento raiz para a configuração ou o recurso que esse cmdlet insere.</span><span class="sxs-lookup"><span data-stu-id="cc17d-125">The XML content must be less than 4 KB and must include the root element for the setting or feature that this cmdlet inserts.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc17d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc17d-126">-DefaultProfile</span></span>
<span data-ttu-id="cc17d-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cc17d-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc17d-128">-SettingName</span><span class="sxs-lookup"><span data-stu-id="cc17d-128">-SettingName</span></span>
<span data-ttu-id="cc17d-129">Especifica o nome da configuração à qual o conteúdo se aplica.</span><span class="sxs-lookup"><span data-stu-id="cc17d-129">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="cc17d-130">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="cc17d-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cc17d-131">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="cc17d-131">FirstLogonCommands</span></span>
- <span data-ttu-id="cc17d-132">Logon automático</span><span class="sxs-lookup"><span data-stu-id="cc17d-132">AutoLogon</span></span>

```yaml
Type: SettingNames
Parameter Sets: (All)
Aliases: 
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc17d-133">-VM</span><span class="sxs-lookup"><span data-stu-id="cc17d-133">-VM</span></span>
<span data-ttu-id="cc17d-134">Especifica o objeto da máquina virtual que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="cc17d-134">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="cc17d-135">Para obter um objeto de máquina virtual, use o cmdlet [Get-AzVM](./Get-AzVM.md) .</span><span class="sxs-lookup"><span data-stu-id="cc17d-135">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="cc17d-136">Crie um objeto de máquina virtual usando o cmdlet [New-AzVMConfig](./New-AzVMConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="cc17d-136">Create a virtual machine object by using the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc17d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc17d-137">CommonParameters</span></span>
<span data-ttu-id="cc17d-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc17d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc17d-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc17d-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc17d-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cc17d-140">INPUTS</span></span>

### <span data-ttu-id="cc17d-141">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="cc17d-141">PSVirtualMachine</span></span>
<span data-ttu-id="cc17d-142">O parâmetro ' VM ' aceita o valor do tipo ' PSVirtualMachine ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="cc17d-142">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="cc17d-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cc17d-143">OUTPUTS</span></span>

### <span data-ttu-id="cc17d-144">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="cc17d-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="cc17d-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cc17d-145">NOTES</span></span>

## <span data-ttu-id="cc17d-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cc17d-146">RELATED LINKS</span></span>

[<span data-ttu-id="cc17d-147">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="cc17d-147">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="cc17d-148">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="cc17d-148">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="cc17d-149">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="cc17d-149">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
