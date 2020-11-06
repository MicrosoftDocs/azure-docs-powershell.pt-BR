---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDiagnosticsExtension.md
ms.openlocfilehash: 0e28b5df77734645380316af6396f745469637df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431717"
---
# <span data-ttu-id="0957b-101">Add-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="0957b-101">Add-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="0957b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0957b-102">SYNOPSIS</span></span>
<span data-ttu-id="0957b-103">Adiciona uma extensão de diagnóstico ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="0957b-103">Adds a diagnostics extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0957b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0957b-104">SYNTAX</span></span>

```
Add-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-SettingFilePath] <String> [[-ProtectedSettingFilePath] <String>] [[-Name] <String>]
 [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0957b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0957b-105">DESCRIPTION</span></span>
<span data-ttu-id="0957b-106">O cmdlet **Add-AzureRmVmssDiagnosticsExtension** adiciona uma extensão de diagnóstico à instância do VMSS (conjunto de dimensionamento de máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="0957b-106">The **Add-AzureRmVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="0957b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0957b-107">EXAMPLES</span></span>

### <span data-ttu-id="0957b-108">Exemplo 1: adicionar uma extensão de diagnóstico ao VMSS</span><span class="sxs-lookup"><span data-stu-id="0957b-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="0957b-109">Esse comando adiciona uma extensão de diagnóstico à VMSS.</span><span class="sxs-lookup"><span data-stu-id="0957b-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="0957b-110">OS</span><span class="sxs-lookup"><span data-stu-id="0957b-110">PARAMETERS</span></span>

### <span data-ttu-id="0957b-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="0957b-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="0957b-112">Indica se esse cmdlet permite que o agente convidado do Azure atualize automaticamente a extensão para uma versão secundária mais recente.</span><span class="sxs-lookup"><span data-stu-id="0957b-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0957b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="0957b-113">-Force</span></span>
<span data-ttu-id="0957b-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="0957b-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0957b-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="0957b-115">-Name</span></span>
<span data-ttu-id="0957b-116">Especifica o nome de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="0957b-116">Specifies the name of an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0957b-117">-ProtectedSettingFilePath</span><span class="sxs-lookup"><span data-stu-id="0957b-117">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="0957b-118">Especifica o caminho do arquivo de configuração particular.</span><span class="sxs-lookup"><span data-stu-id="0957b-118">Specifies the path of the private configuration file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0957b-119">-SettingFilePath</span><span class="sxs-lookup"><span data-stu-id="0957b-119">-SettingFilePath</span></span>
<span data-ttu-id="0957b-120">Especifica o caminho do arquivo de configuração pública.</span><span class="sxs-lookup"><span data-stu-id="0957b-120">Specifies the path of the public configuration file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0957b-121">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="0957b-121">-TypeHandlerVersion</span></span>
<span data-ttu-id="0957b-122">Especifica a versão da extensão a ser usada para este VMSS.</span><span class="sxs-lookup"><span data-stu-id="0957b-122">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="0957b-123">Para obter a versão, execute o cmdlet [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) com um valor de Microsoft. Azure. Diagnostics para o parâmetro *PublisherName* e IaaSDiagnostics para o parâmetro de *tipo* .</span><span class="sxs-lookup"><span data-stu-id="0957b-123">To obtain the version, run the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0957b-124">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0957b-124">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="0957b-125">Especifique o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="0957b-125">Specify the VMSS object.</span></span>
<span data-ttu-id="0957b-126">Você pode usar o cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="0957b-126">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="0957b-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0957b-127">-Confirm</span></span>
<span data-ttu-id="0957b-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0957b-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0957b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0957b-129">-WhatIf</span></span>
<span data-ttu-id="0957b-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0957b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0957b-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0957b-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0957b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0957b-132">CommonParameters</span></span>
<span data-ttu-id="0957b-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0957b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0957b-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0957b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0957b-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0957b-135">INPUTS</span></span>

### <span data-ttu-id="0957b-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0957b-136">None</span></span>
<span data-ttu-id="0957b-137">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="0957b-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0957b-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0957b-138">OUTPUTS</span></span>

###  
<span data-ttu-id="0957b-139">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="0957b-139">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="0957b-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0957b-140">NOTES</span></span>

## <span data-ttu-id="0957b-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0957b-141">RELATED LINKS</span></span>

[<span data-ttu-id="0957b-142">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="0957b-142">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="0957b-143">Remove-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="0957b-143">Remove-AzureRmVmssDiagnosticsExtension</span></span>](./Remove-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="0957b-144">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="0957b-144">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)
