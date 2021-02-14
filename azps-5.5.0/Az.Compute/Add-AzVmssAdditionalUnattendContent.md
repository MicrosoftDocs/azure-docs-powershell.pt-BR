---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
ms.openlocfilehash: 051228464b2f1e9770507ceacd4eaabfce5236b1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111162"
---
# <span data-ttu-id="1e613-101">Add-AzVmssAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="1e613-101">Add-AzVmssAdditionalUnattendContent</span></span>

## <span data-ttu-id="1e613-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1e613-102">SYNOPSIS</span></span>
<span data-ttu-id="1e613-103">Adiciona informações ao arquivo de resposta de configuração autônoma do Windows.</span><span class="sxs-lookup"><span data-stu-id="1e613-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="1e613-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1e613-104">SYNTAX</span></span>

```
Add-AzVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e613-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="1e613-105">DESCRIPTION</span></span>
<span data-ttu-id="1e613-106">O cmdlet **Add-AzVmssAdditionalUnattendContent** adiciona informações ao arquivo de resposta de configuração autônoma do Windows.</span><span class="sxs-lookup"><span data-stu-id="1e613-106">The **Add-AzVmssAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="1e613-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1e613-107">EXAMPLES</span></span>

### <span data-ttu-id="1e613-108">Exemplo 1: Adicionar informações ao arquivo de resposta de configuração autônoma do Windows</span><span class="sxs-lookup"><span data-stu-id="1e613-108">Example 1: Add information to the unattended Windows Setup answer file</span></span>
```
PS C:\> Add-AzVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

<span data-ttu-id="1e613-109">Esse comando adiciona informações ao arquivo de resposta de configuração autônoma do Windows.</span><span class="sxs-lookup"><span data-stu-id="1e613-109">This command adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="1e613-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1e613-110">PARAMETERS</span></span>

### <span data-ttu-id="1e613-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="1e613-111">-ComponentName</span></span>
<span data-ttu-id="1e613-112">Especifica o nome do componente a ser definido com o conteúdo adicionado.</span><span class="sxs-lookup"><span data-stu-id="1e613-112">Specifies the name of the component to configure with the added content.</span></span>
<span data-ttu-id="1e613-113">O único valor que pode ser possível é o Microsoft-Windows-Shell-Setup.</span><span class="sxs-lookup"><span data-stu-id="1e613-113">The only allowable value is Microsoft-Windows-Shell-Setup.</span></span>

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

### <span data-ttu-id="1e613-114">-Conteúdo</span><span class="sxs-lookup"><span data-stu-id="1e613-114">-Content</span></span>
<span data-ttu-id="1e613-115">Especifica o conteúdo formatado xml que é adicionado ao arquivo unattend.xml para o caminho e componente especificados.</span><span class="sxs-lookup"><span data-stu-id="1e613-115">Specifies the XML formatted content that is added to the unattend.xml file for the specified path and component.</span></span>

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

### <span data-ttu-id="1e613-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e613-116">-DefaultProfile</span></span>
<span data-ttu-id="1e613-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="1e613-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e613-118">-NomeDoPasso</span><span class="sxs-lookup"><span data-stu-id="1e613-118">-PassName</span></span>
<span data-ttu-id="1e613-119">Especifica o nome do passe ao que o conteúdo se aplica.</span><span class="sxs-lookup"><span data-stu-id="1e613-119">Specifies the name of the pass that the content applies to.</span></span>
<span data-ttu-id="1e613-120">O único valor possível é oobeSystem.</span><span class="sxs-lookup"><span data-stu-id="1e613-120">The only allowable value is oobeSystem.</span></span>

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

### <span data-ttu-id="1e613-121">-SettingName</span><span class="sxs-lookup"><span data-stu-id="1e613-121">-SettingName</span></span>
<span data-ttu-id="1e613-122">Especifica o nome da configuração à qual o conteúdo se aplica.</span><span class="sxs-lookup"><span data-stu-id="1e613-122">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="1e613-123">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="1e613-123">The acceptable values for this parameter are::</span></span>
- <span data-ttu-id="1e613-124">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="1e613-124">FirstLogonCommands</span></span>
- <span data-ttu-id="1e613-125">Autologon</span><span class="sxs-lookup"><span data-stu-id="1e613-125">AutoLogon</span></span>

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

### <span data-ttu-id="1e613-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1e613-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="1e613-127">Especifique o objeto **Conjunto de Escala da máquina** virtual.</span><span class="sxs-lookup"><span data-stu-id="1e613-127">Specify the virtual machine **Scale Set** object.</span></span>
<span data-ttu-id="1e613-128">Você pode usar [o cmdlet New-AzVmssConfig](./New-AzVmssConfig.md) para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="1e613-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="1e613-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="1e613-129">-Confirm</span></span>
<span data-ttu-id="1e613-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e613-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e613-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e613-131">-WhatIf</span></span>
<span data-ttu-id="1e613-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1e613-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1e613-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1e613-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e613-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e613-134">CommonParameters</span></span>
<span data-ttu-id="1e613-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e613-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e613-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1e613-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e613-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="1e613-137">INPUTS</span></span>

### <span data-ttu-id="1e613-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1e613-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="1e613-139">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.PassNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="1e613-139">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.PassNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="1e613-140">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.ComponentNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="1e613-140">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ComponentNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="1e613-141">System.Nullable'1[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="1e613-141">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="1e613-142">System.String</span><span class="sxs-lookup"><span data-stu-id="1e613-142">System.String</span></span>

## <span data-ttu-id="1e613-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="1e613-143">OUTPUTS</span></span>

### <span data-ttu-id="1e613-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1e613-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="1e613-145">Notas</span><span class="sxs-lookup"><span data-stu-id="1e613-145">NOTES</span></span>

## <span data-ttu-id="1e613-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1e613-146">RELATED LINKS</span></span>

[<span data-ttu-id="1e613-147">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="1e613-147">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
