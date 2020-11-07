---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: f84d9f823d97872d8ad2491a2ab45ef3bb5a22a7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93777080"
---
# <span data-ttu-id="ab0c3-101">Add-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="ab0c3-101">Add-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="ab0c3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ab0c3-102">SYNOPSIS</span></span>
<span data-ttu-id="ab0c3-103">Adiciona uma extensão de diagnóstico ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="ab0c3-103">Adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="ab0c3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ab0c3-104">SYNTAX</span></span>

```
Add-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-SettingFilePath] <String> [[-ProtectedSettingFilePath] <String>] [[-Name] <String>]
 [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab0c3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ab0c3-105">DESCRIPTION</span></span>
<span data-ttu-id="ab0c3-106">O cmdlet **Add-AzVmssDiagnosticsExtension** adiciona uma extensão de diagnóstico à instância do VMSS (conjunto de dimensionamento de máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="ab0c3-106">The **Add-AzVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="ab0c3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ab0c3-107">EXAMPLES</span></span>

### <span data-ttu-id="ab0c3-108">Exemplo 1: adicionar uma extensão de diagnóstico ao VMSS</span><span class="sxs-lookup"><span data-stu-id="ab0c3-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="ab0c3-109">Esse comando adiciona uma extensão de diagnóstico à VMSS.</span><span class="sxs-lookup"><span data-stu-id="ab0c3-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="ab0c3-110">OS</span><span class="sxs-lookup"><span data-stu-id="ab0c3-110">PARAMETERS</span></span>

### <span data-ttu-id="ab0c3-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="ab0c3-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="ab0c3-112">Indica se esse cmdlet permite que o agente convidado do Azure atualize automaticamente a extensão para uma versão secundária mais recente.</span><span class="sxs-lookup"><span data-stu-id="ab0c3-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

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

### <span data-ttu-id="ab0c3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab0c3-113">-DefaultProfile</span></span>
<span data-ttu-id="ab0c3-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ab0c3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab0c3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ab0c3-115">-Force</span></span>
<span data-ttu-id="ab0c3-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="ab0c3-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ab0c3-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ab0c3-117">-Name</span></span>
<span data-ttu-id="ab0c3-118">Especifica o nome de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="ab0c3-118">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="ab0c3-119">-ProtectedSettingFilePath</span><span class="sxs-lookup"><span data-stu-id="ab0c3-119">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="ab0c3-120">Especifica o caminho do arquivo de configuração particular.</span><span class="sxs-lookup"><span data-stu-id="ab0c3-120">Specifies the path of the private configuration file.</span></span>

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

### <span data-ttu-id="ab0c3-121">-SettingFilePath</span><span class="sxs-lookup"><span data-stu-id="ab0c3-121">-SettingFilePath</span></span>
<span data-ttu-id="ab0c3-122">Especifica o caminho do arquivo de configuração pública.</span><span class="sxs-lookup"><span data-stu-id="ab0c3-122">Specifies the path of the public configuration file.</span></span>

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

### <span data-ttu-id="ab0c3-123">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="ab0c3-123">-TypeHandlerVersion</span></span>
<span data-ttu-id="ab0c3-124">Especifica a versão da extensão a ser usada para este VMSS.</span><span class="sxs-lookup"><span data-stu-id="ab0c3-124">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="ab0c3-125">Para obter a versão, execute o cmdlet [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) com um valor de Microsoft. Azure. Diagnostics para o parâmetro *PublisherName* e IaaSDiagnostics para o parâmetro de *tipo* .</span><span class="sxs-lookup"><span data-stu-id="ab0c3-125">To obtain the version, run the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

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

### <span data-ttu-id="ab0c3-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ab0c3-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="ab0c3-127">Especifique o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="ab0c3-127">Specify the VMSS object.</span></span>
<span data-ttu-id="ab0c3-128">Você pode usar o cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="ab0c3-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="ab0c3-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ab0c3-129">-Confirm</span></span>
<span data-ttu-id="ab0c3-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab0c3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab0c3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab0c3-131">-WhatIf</span></span>
<span data-ttu-id="ab0c3-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ab0c3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab0c3-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ab0c3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab0c3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab0c3-134">CommonParameters</span></span>
<span data-ttu-id="ab0c3-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab0c3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab0c3-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab0c3-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab0c3-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ab0c3-137">INPUTS</span></span>

### <span data-ttu-id="ab0c3-138">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ab0c3-138">VirtualMachineScaleSet</span></span>
<span data-ttu-id="ab0c3-139">O parâmetro ' VirtualMachineScaleSet ' aceita o valor do tipo ' VirtualMachineScaleSet ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="ab0c3-139">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="ab0c3-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ab0c3-140">OUTPUTS</span></span>

###  
<span data-ttu-id="ab0c3-141">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="ab0c3-141">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="ab0c3-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ab0c3-142">NOTES</span></span>

## <span data-ttu-id="ab0c3-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ab0c3-143">RELATED LINKS</span></span>

[<span data-ttu-id="ab0c3-144">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="ab0c3-144">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="ab0c3-145">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="ab0c3-145">Remove-AzVmssDiagnosticsExtension</span></span>](./Remove-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="ab0c3-146">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="ab0c3-146">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)
