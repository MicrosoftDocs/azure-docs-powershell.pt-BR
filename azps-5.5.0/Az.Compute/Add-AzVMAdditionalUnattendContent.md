---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
ms.openlocfilehash: 05f100e730cb808bf40bbec60386901eb39020ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117884"
---
# <span data-ttu-id="1435c-101">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="1435c-101">Add-AzVMAdditionalUnattendContent</span></span>

## <span data-ttu-id="1435c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1435c-102">SYNOPSIS</span></span>
<span data-ttu-id="1435c-103">Adiciona informações ao arquivo de resposta de configuração autônoma do Windows.</span><span class="sxs-lookup"><span data-stu-id="1435c-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="1435c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1435c-104">SYNTAX</span></span>

```
Add-AzVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1435c-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="1435c-105">DESCRIPTION</span></span>
<span data-ttu-id="1435c-106">O **cmdlet Add-AzVMAdditionalUnattendContent** adiciona informações ao arquivo de resposta de configuração autônoma do Windows.</span><span class="sxs-lookup"><span data-stu-id="1435c-106">The **Add-AzVMAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>
<span data-ttu-id="1435c-107">Especifique informações adicionais codificadas .xml codificadas de base 64 que este cmdlet adiciona ao arquivo unattend.xml arquivo.</span><span class="sxs-lookup"><span data-stu-id="1435c-107">Specify additional base 64 encoded .xml formatted information that this cmdlet adds to the unattend.xml file.</span></span>

## <span data-ttu-id="1435c-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1435c-108">EXAMPLES</span></span>

### <span data-ttu-id="1435c-109">Exemplo 1: Adicionar conteúdo ao unattend.xml</span><span class="sxs-lookup"><span data-stu-id="1435c-109">Example 1: Add content to unattend.xml</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

<span data-ttu-id="1435c-110">O primeiro comando obtém o conjunto de disponibilidade chamado AvailabilitySet03 no grupo de recursos chamado ResourceGroup11 e armazena esse objeto na variável $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="1435c-110">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="1435c-111">O segundo comando cria um objeto virtual de máquina e o armazena na variável $VirtualMachine dados.</span><span class="sxs-lookup"><span data-stu-id="1435c-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="1435c-112">O comando atribui um nome e um tamanho à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1435c-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="1435c-113">A máquina virtual pertence ao conjunto de disponibilidade armazenado em $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="1435c-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="1435c-114">O terceiro comando cria um objeto de credencial usando o cmdlet Get-Credential e armazena o resultado na variável $Credential dados.</span><span class="sxs-lookup"><span data-stu-id="1435c-114">The third command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="1435c-115">O comando solicita um nome de usuário e senha.</span><span class="sxs-lookup"><span data-stu-id="1435c-115">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="1435c-116">Para obter mais informações, digite `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="1435c-116">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="1435c-117">O quarto comando usa **o cmdlet Set-AzVMOperatingSystem** para configurar a máquina virtual armazenada no $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="1435c-117">The fourth command uses the **Set-AzVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="1435c-118">O quinto comando atribui conteúdo à variável $AucContent dados.</span><span class="sxs-lookup"><span data-stu-id="1435c-118">The fifth command assigns content to the $AucContent variable.</span></span>
<span data-ttu-id="1435c-119">O conteúdo inclui uma senha.</span><span class="sxs-lookup"><span data-stu-id="1435c-119">The content includes a password.</span></span>
<span data-ttu-id="1435c-120">O comando final adiciona o conteúdo armazenado no $AucContent ao unattend.xml arquivo.</span><span class="sxs-lookup"><span data-stu-id="1435c-120">The final command adds the content stored in $AucContent to the unattend.xml file.</span></span>

## <span data-ttu-id="1435c-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1435c-121">PARAMETERS</span></span>

### <span data-ttu-id="1435c-122">-Conteúdo</span><span class="sxs-lookup"><span data-stu-id="1435c-122">-Content</span></span>
<span data-ttu-id="1435c-123">Especifica o conteúdo xml codificado da base 64.</span><span class="sxs-lookup"><span data-stu-id="1435c-123">Specifies base 64 encoded XML formatted content.</span></span>
<span data-ttu-id="1435c-124">Este cmdlet adiciona o conteúdo ao arquivo unattend.xml arquivo.</span><span class="sxs-lookup"><span data-stu-id="1435c-124">This cmdlet adds the content to the unattend.xml file.</span></span>
<span data-ttu-id="1435c-125">O conteúdo XML deve ser menor que 4 KB e deve incluir o elemento raiz para a configuração ou recurso que esse cmdlet insere.</span><span class="sxs-lookup"><span data-stu-id="1435c-125">The XML content must be less than 4 KB and must include the root element for the setting or feature that this cmdlet inserts.</span></span>

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

### <span data-ttu-id="1435c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1435c-126">-DefaultProfile</span></span>
<span data-ttu-id="1435c-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="1435c-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1435c-128">-SettingName</span><span class="sxs-lookup"><span data-stu-id="1435c-128">-SettingName</span></span>
<span data-ttu-id="1435c-129">Especifica o nome da configuração à qual o conteúdo se aplica.</span><span class="sxs-lookup"><span data-stu-id="1435c-129">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="1435c-130">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="1435c-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1435c-131">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="1435c-131">FirstLogonCommands</span></span>
- <span data-ttu-id="1435c-132">Autologon</span><span class="sxs-lookup"><span data-stu-id="1435c-132">AutoLogon</span></span>

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

### <span data-ttu-id="1435c-133">-VM</span><span class="sxs-lookup"><span data-stu-id="1435c-133">-VM</span></span>
<span data-ttu-id="1435c-134">Especifica o objeto de máquina virtual que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="1435c-134">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="1435c-135">Para obter um objeto de máquina virtual, use [o cmdlet Get-AzVM.](./Get-AzVM.md)</span><span class="sxs-lookup"><span data-stu-id="1435c-135">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="1435c-136">Crie um objeto de máquina virtual usando [o cmdlet New-AzVMConfig.](./New-AzVMConfig.md)</span><span class="sxs-lookup"><span data-stu-id="1435c-136">Create a virtual machine object by using the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet.</span></span>

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

### <span data-ttu-id="1435c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1435c-137">CommonParameters</span></span>
<span data-ttu-id="1435c-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1435c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1435c-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1435c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1435c-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="1435c-140">INPUTS</span></span>

### <span data-ttu-id="1435c-141">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="1435c-141">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="1435c-142">System.String</span><span class="sxs-lookup"><span data-stu-id="1435c-142">System.String</span></span>

### <span data-ttu-id="1435c-143">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="1435c-143">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="1435c-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="1435c-144">OUTPUTS</span></span>

### <span data-ttu-id="1435c-145">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="1435c-145">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="1435c-146">Notas</span><span class="sxs-lookup"><span data-stu-id="1435c-146">NOTES</span></span>

## <span data-ttu-id="1435c-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1435c-147">RELATED LINKS</span></span>

[<span data-ttu-id="1435c-148">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1435c-148">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="1435c-149">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="1435c-149">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="1435c-150">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="1435c-150">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
