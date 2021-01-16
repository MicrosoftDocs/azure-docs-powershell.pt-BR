---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
ms.openlocfilehash: 051228464b2f1e9770507ceacd4eaabfce5236b1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261384"
---
# <span data-ttu-id="75e47-101">Add-AzVmssAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="75e47-101">Add-AzVmssAdditionalUnattendContent</span></span>

## <span data-ttu-id="75e47-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75e47-102">SYNOPSIS</span></span>
<span data-ttu-id="75e47-103">Adiciona informações ao arquivo de resposta da instalação autônoma do Windows.</span><span class="sxs-lookup"><span data-stu-id="75e47-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="75e47-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75e47-104">SYNTAX</span></span>

```
Add-AzVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75e47-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="75e47-105">DESCRIPTION</span></span>
<span data-ttu-id="75e47-106">O cmdlet **Add-AzVmssAdditionalUnattendContent** adiciona informações ao arquivo de resposta da instalação autônoma do Windows.</span><span class="sxs-lookup"><span data-stu-id="75e47-106">The **Add-AzVmssAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="75e47-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="75e47-107">EXAMPLES</span></span>

### <span data-ttu-id="75e47-108">Exemplo 1: adicionar informações ao arquivo de resposta da instalação autônoma do Windows</span><span class="sxs-lookup"><span data-stu-id="75e47-108">Example 1: Add information to the unattended Windows Setup answer file</span></span>
```
PS C:\> Add-AzVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

<span data-ttu-id="75e47-109">Esse comando adiciona informações ao arquivo de resposta da instalação autônoma do Windows.</span><span class="sxs-lookup"><span data-stu-id="75e47-109">This command adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="75e47-110">OS</span><span class="sxs-lookup"><span data-stu-id="75e47-110">PARAMETERS</span></span>

### <span data-ttu-id="75e47-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="75e47-111">-ComponentName</span></span>
<span data-ttu-id="75e47-112">Especifica o nome do componente a ser configurado com o conteúdo adicionado.</span><span class="sxs-lookup"><span data-stu-id="75e47-112">Specifies the name of the component to configure with the added content.</span></span>
<span data-ttu-id="75e47-113">O único valor permitido é Microsoft-Windows-Shell-Setup.</span><span class="sxs-lookup"><span data-stu-id="75e47-113">The only allowable value is Microsoft-Windows-Shell-Setup.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ComponentNames]
Parameter Sets: (All)
Aliases:
Accepted values: MicrosoftWindowsShellSetup

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75e47-114">-Conteúdo</span><span class="sxs-lookup"><span data-stu-id="75e47-114">-Content</span></span>
<span data-ttu-id="75e47-115">Especifica o conteúdo formatado em XML que é adicionado ao arquivo unattend.xml para o caminho e componente especificados.</span><span class="sxs-lookup"><span data-stu-id="75e47-115">Specifies the XML formatted content that is added to the unattend.xml file for the specified path and component.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75e47-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75e47-116">-DefaultProfile</span></span>
<span data-ttu-id="75e47-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="75e47-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75e47-118">-Passname</span><span class="sxs-lookup"><span data-stu-id="75e47-118">-PassName</span></span>
<span data-ttu-id="75e47-119">Especifica o nome da passagem à qual o conteúdo se aplica.</span><span class="sxs-lookup"><span data-stu-id="75e47-119">Specifies the name of the pass that the content applies to.</span></span>
<span data-ttu-id="75e47-120">O único valor permitido é oobeSystem.</span><span class="sxs-lookup"><span data-stu-id="75e47-120">The only allowable value is oobeSystem.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.PassNames]
Parameter Sets: (All)
Aliases:
Accepted values: OobeSystem

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75e47-121">-SettingName</span><span class="sxs-lookup"><span data-stu-id="75e47-121">-SettingName</span></span>
<span data-ttu-id="75e47-122">Especifica o nome da configuração à qual o conteúdo se aplica.</span><span class="sxs-lookup"><span data-stu-id="75e47-122">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="75e47-123">Os valores aceitáveis para esse parâmetro são::</span><span class="sxs-lookup"><span data-stu-id="75e47-123">The acceptable values for this parameter are::</span></span>
- <span data-ttu-id="75e47-124">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="75e47-124">FirstLogonCommands</span></span>
- <span data-ttu-id="75e47-125">Logon automático</span><span class="sxs-lookup"><span data-stu-id="75e47-125">AutoLogon</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.SettingNames]
Parameter Sets: (All)
Aliases:
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75e47-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="75e47-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="75e47-127">Especifique o objeto do **conjunto de escala** da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="75e47-127">Specify the virtual machine **Scale Set** object.</span></span>
<span data-ttu-id="75e47-128">Você pode usar o cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="75e47-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75e47-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="75e47-129">-Confirm</span></span>
<span data-ttu-id="75e47-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75e47-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75e47-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75e47-131">-WhatIf</span></span>
<span data-ttu-id="75e47-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="75e47-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75e47-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="75e47-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75e47-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75e47-134">CommonParameters</span></span>
<span data-ttu-id="75e47-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75e47-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75e47-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75e47-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75e47-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="75e47-137">INPUTS</span></span>

### <span data-ttu-id="75e47-138">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="75e47-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="75e47-139">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. Models. Passnames, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="75e47-139">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.PassNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="75e47-140">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. Models. Componentnames, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="75e47-140">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ComponentNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="75e47-141">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. Models. Settingnames, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="75e47-141">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="75e47-142">System. String</span><span class="sxs-lookup"><span data-stu-id="75e47-142">System.String</span></span>

## <span data-ttu-id="75e47-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="75e47-143">OUTPUTS</span></span>

### <span data-ttu-id="75e47-144">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="75e47-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="75e47-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="75e47-145">NOTES</span></span>

## <span data-ttu-id="75e47-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75e47-146">RELATED LINKS</span></span>

[<span data-ttu-id="75e47-147">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="75e47-147">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
