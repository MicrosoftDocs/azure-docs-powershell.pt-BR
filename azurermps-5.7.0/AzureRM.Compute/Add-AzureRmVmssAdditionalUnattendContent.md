---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssAdditionalUnattendContent.md
ms.openlocfilehash: de61efcbabb2e5acd7d82bf7a1cec8341fe06433
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428985"
---
# <span data-ttu-id="9d1aa-101">Add-AzureRmVmssAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="9d1aa-101">Add-AzureRmVmssAdditionalUnattendContent</span></span>

## <span data-ttu-id="9d1aa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9d1aa-102">SYNOPSIS</span></span>
<span data-ttu-id="9d1aa-103">Adiciona informações ao arquivo de resposta da instalação autônoma do Windows.</span><span class="sxs-lookup"><span data-stu-id="9d1aa-103">Adds information to the unattended Windows Setup answer file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d1aa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9d1aa-104">SYNTAX</span></span>

```
Add-AzureRmVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d1aa-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9d1aa-105">DESCRIPTION</span></span>
<span data-ttu-id="9d1aa-106">O cmdlet **Add-AzureRmVmssAdditionalUnattendContent** adiciona informações ao arquivo de resposta da instalação autônoma do Windows.</span><span class="sxs-lookup"><span data-stu-id="9d1aa-106">The **Add-AzureRmVmssAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="9d1aa-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9d1aa-107">EXAMPLES</span></span>

### <span data-ttu-id="9d1aa-108">Exemplo 1: adicionar informações ao arquivo de resposta da instalação autônoma do Windows</span><span class="sxs-lookup"><span data-stu-id="9d1aa-108">Example 1: Add information to the unattended Windows Setup answer file</span></span>
```
PS C:\> Add-AzureRmVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

<span data-ttu-id="9d1aa-109">Esse comando adiciona informações ao arquivo de resposta da instalação autônoma do Windows.</span><span class="sxs-lookup"><span data-stu-id="9d1aa-109">This command adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="9d1aa-110">OS</span><span class="sxs-lookup"><span data-stu-id="9d1aa-110">PARAMETERS</span></span>

### <span data-ttu-id="9d1aa-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="9d1aa-111">-ComponentName</span></span>
<span data-ttu-id="9d1aa-112">Especifica o nome do componente a ser configurado com o conteúdo adicionado.</span><span class="sxs-lookup"><span data-stu-id="9d1aa-112">Specifies the name of the component to configure with the added content.</span></span>
<span data-ttu-id="9d1aa-113">O único valor permitido é Microsoft-Windows-Shell-Setup.</span><span class="sxs-lookup"><span data-stu-id="9d1aa-113">The only allowable value is Microsoft-Windows-Shell-Setup.</span></span>

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

### <span data-ttu-id="9d1aa-114">-Conteúdo</span><span class="sxs-lookup"><span data-stu-id="9d1aa-114">-Content</span></span>
<span data-ttu-id="9d1aa-115">Especifica o conteúdo formatado em XML que é adicionado ao arquivo unattend.xml para o caminho e componente especificados.</span><span class="sxs-lookup"><span data-stu-id="9d1aa-115">Specifies the XML formatted content that is added to the unattend.xml file for the specified path and component.</span></span>

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

### <span data-ttu-id="9d1aa-116">-Passname</span><span class="sxs-lookup"><span data-stu-id="9d1aa-116">-PassName</span></span>
<span data-ttu-id="9d1aa-117">Especifica o nome da passagem à qual o conteúdo se aplica.</span><span class="sxs-lookup"><span data-stu-id="9d1aa-117">Specifies the name of the pass that the content applies to.</span></span>
<span data-ttu-id="9d1aa-118">O único valor permitido é oobeSystem.</span><span class="sxs-lookup"><span data-stu-id="9d1aa-118">The only allowable value is oobeSystem.</span></span>

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

### <span data-ttu-id="9d1aa-119">-SettingName</span><span class="sxs-lookup"><span data-stu-id="9d1aa-119">-SettingName</span></span>
<span data-ttu-id="9d1aa-120">Especifica o nome da configuração à qual o conteúdo se aplica.</span><span class="sxs-lookup"><span data-stu-id="9d1aa-120">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="9d1aa-121">Os valores aceitáveis para esse parâmetro são::</span><span class="sxs-lookup"><span data-stu-id="9d1aa-121">The acceptable values for this parameter are::</span></span>

- <span data-ttu-id="9d1aa-122">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="9d1aa-122">FirstLogonCommands</span></span>
- <span data-ttu-id="9d1aa-123">Logon automático</span><span class="sxs-lookup"><span data-stu-id="9d1aa-123">AutoLogon</span></span>

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

### <span data-ttu-id="9d1aa-124">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9d1aa-124">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="9d1aa-125">Especifique o objeto do **conjunto de escala** da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9d1aa-125">Specify the virtual machine **Scale Set** object.</span></span>
<span data-ttu-id="9d1aa-126">Você pode usar o cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="9d1aa-126">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d1aa-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9d1aa-127">-Confirm</span></span>
<span data-ttu-id="9d1aa-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d1aa-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d1aa-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d1aa-129">-WhatIf</span></span>
<span data-ttu-id="9d1aa-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9d1aa-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9d1aa-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9d1aa-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d1aa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d1aa-132">CommonParameters</span></span>
<span data-ttu-id="9d1aa-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d1aa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d1aa-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d1aa-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d1aa-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9d1aa-135">INPUTS</span></span>

### <span data-ttu-id="9d1aa-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9d1aa-136">None</span></span>
<span data-ttu-id="9d1aa-137">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="9d1aa-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9d1aa-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9d1aa-138">OUTPUTS</span></span>

## <span data-ttu-id="9d1aa-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9d1aa-139">NOTES</span></span>

## <span data-ttu-id="9d1aa-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9d1aa-140">RELATED LINKS</span></span>

[<span data-ttu-id="9d1aa-141">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="9d1aa-141">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
