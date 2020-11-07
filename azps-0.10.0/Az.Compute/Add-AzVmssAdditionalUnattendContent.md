---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
ms.openlocfilehash: 38f510602259ca799c6df947b9d74984dff178ba
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93777089"
---
# <span data-ttu-id="36390-101">Add-AzVmssAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="36390-101">Add-AzVmssAdditionalUnattendContent</span></span>

## <span data-ttu-id="36390-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="36390-102">SYNOPSIS</span></span>
<span data-ttu-id="36390-103">Adiciona informações ao arquivo de resposta da instalação autônoma do Windows.</span><span class="sxs-lookup"><span data-stu-id="36390-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="36390-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36390-104">SYNTAX</span></span>

```
Add-AzVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36390-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="36390-105">DESCRIPTION</span></span>
<span data-ttu-id="36390-106">O cmdlet **Add-AzVmssAdditionalUnattendContent** adiciona informações ao arquivo de resposta da instalação autônoma do Windows.</span><span class="sxs-lookup"><span data-stu-id="36390-106">The **Add-AzVmssAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="36390-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="36390-107">EXAMPLES</span></span>

### <span data-ttu-id="36390-108">Exemplo 1: adicionar informações ao arquivo de resposta da instalação autônoma do Windows</span><span class="sxs-lookup"><span data-stu-id="36390-108">Example 1: Add information to the unattended Windows Setup answer file</span></span>
```
PS C:\> Add-AzVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

<span data-ttu-id="36390-109">Esse comando adiciona informações ao arquivo de resposta da instalação autônoma do Windows.</span><span class="sxs-lookup"><span data-stu-id="36390-109">This command adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="36390-110">OS</span><span class="sxs-lookup"><span data-stu-id="36390-110">PARAMETERS</span></span>

### <span data-ttu-id="36390-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="36390-111">-ComponentName</span></span>
<span data-ttu-id="36390-112">Especifica o nome do componente a ser configurado com o conteúdo adicionado.</span><span class="sxs-lookup"><span data-stu-id="36390-112">Specifies the name of the component to configure with the added content.</span></span>
<span data-ttu-id="36390-113">O único valor permitido é Microsoft-Windows-Shell-Setup.</span><span class="sxs-lookup"><span data-stu-id="36390-113">The only allowable value is Microsoft-Windows-Shell-Setup.</span></span>

```yaml
Type: ComponentNames
Parameter Sets: (All)
Aliases: 
Accepted values: MicrosoftWindowsShellSetup

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36390-114">-Conteúdo</span><span class="sxs-lookup"><span data-stu-id="36390-114">-Content</span></span>
<span data-ttu-id="36390-115">Especifica o conteúdo formatado em XML que é adicionado ao arquivo unattend.xml para o caminho e componente especificados.</span><span class="sxs-lookup"><span data-stu-id="36390-115">Specifies the XML formatted content that is added to the unattend.xml file for the specified path and component.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36390-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36390-116">-DefaultProfile</span></span>
<span data-ttu-id="36390-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="36390-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36390-118">-Passname</span><span class="sxs-lookup"><span data-stu-id="36390-118">-PassName</span></span>
<span data-ttu-id="36390-119">Especifica o nome da passagem à qual o conteúdo se aplica.</span><span class="sxs-lookup"><span data-stu-id="36390-119">Specifies the name of the pass that the content applies to.</span></span>
<span data-ttu-id="36390-120">O único valor permitido é oobeSystem.</span><span class="sxs-lookup"><span data-stu-id="36390-120">The only allowable value is oobeSystem.</span></span>

```yaml
Type: PassNames
Parameter Sets: (All)
Aliases: 
Accepted values: OobeSystem

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36390-121">-SettingName</span><span class="sxs-lookup"><span data-stu-id="36390-121">-SettingName</span></span>
<span data-ttu-id="36390-122">Especifica o nome da configuração à qual o conteúdo se aplica.</span><span class="sxs-lookup"><span data-stu-id="36390-122">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="36390-123">Os valores aceitáveis para esse parâmetro são::</span><span class="sxs-lookup"><span data-stu-id="36390-123">The acceptable values for this parameter are::</span></span>

- <span data-ttu-id="36390-124">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="36390-124">FirstLogonCommands</span></span>
- <span data-ttu-id="36390-125">Logon automático</span><span class="sxs-lookup"><span data-stu-id="36390-125">AutoLogon</span></span>

```yaml
Type: SettingNames
Parameter Sets: (All)
Aliases: 
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36390-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="36390-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="36390-127">Especifique o objeto do **conjunto de escala** da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="36390-127">Specify the virtual machine **Scale Set** object.</span></span>
<span data-ttu-id="36390-128">Você pode usar o cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="36390-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36390-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="36390-129">-Confirm</span></span>
<span data-ttu-id="36390-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36390-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36390-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36390-131">-WhatIf</span></span>
<span data-ttu-id="36390-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="36390-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36390-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="36390-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36390-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36390-134">CommonParameters</span></span>
<span data-ttu-id="36390-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36390-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36390-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36390-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36390-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="36390-137">INPUTS</span></span>

### <span data-ttu-id="36390-138">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="36390-138">VirtualMachineScaleSet</span></span>
<span data-ttu-id="36390-139">O parâmetro ' VirtualMachineScaleSet ' aceita o valor do tipo ' VirtualMachineScaleSet ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="36390-139">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="36390-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="36390-140">OUTPUTS</span></span>

### <span data-ttu-id="36390-141">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="36390-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="36390-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="36390-142">NOTES</span></span>

## <span data-ttu-id="36390-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="36390-143">RELATED LINKS</span></span>

[<span data-ttu-id="36390-144">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="36390-144">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
