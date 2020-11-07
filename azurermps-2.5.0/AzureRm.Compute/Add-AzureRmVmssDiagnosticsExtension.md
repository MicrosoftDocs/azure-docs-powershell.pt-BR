---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssdiagnosticsextension
schema: 2.0.0
ms.openlocfilehash: 8e6a0ec7002f211e660c3ca71d190faf719bbd6c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785376"
---
# <span data-ttu-id="7c9a2-101">Add-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="7c9a2-101">Add-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="7c9a2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7c9a2-102">SYNOPSIS</span></span>
<span data-ttu-id="7c9a2-103">Adiciona uma extensão de diagnóstico ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="7c9a2-103">Adds a diagnostics extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c9a2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7c9a2-104">SYNTAX</span></span>

```
Add-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-SettingFilePath] <String> [[-ProtectedSettingFilePath] <String>] [[-Name] <String>]
 [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c9a2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7c9a2-105">DESCRIPTION</span></span>
<span data-ttu-id="7c9a2-106">O cmdlet **Add-AzureRmVmssDiagnosticsExtension** adiciona uma extensão de diagnóstico à instância do VMSS (conjunto de dimensionamento de máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="7c9a2-106">The **Add-AzureRmVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="7c9a2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7c9a2-107">EXAMPLES</span></span>

### <span data-ttu-id="7c9a2-108">Exemplo 1: adicionar uma extensão de diagnóstico ao VMSS</span><span class="sxs-lookup"><span data-stu-id="7c9a2-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="7c9a2-109">Esse comando adiciona uma extensão de diagnóstico à VMSS.</span><span class="sxs-lookup"><span data-stu-id="7c9a2-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="7c9a2-110">OS</span><span class="sxs-lookup"><span data-stu-id="7c9a2-110">PARAMETERS</span></span>

### <span data-ttu-id="7c9a2-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="7c9a2-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="7c9a2-112">Indica se esse cmdlet permite que o agente convidado do Azure atualize automaticamente a extensão para uma versão secundária mais recente.</span><span class="sxs-lookup"><span data-stu-id="7c9a2-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

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

### <span data-ttu-id="7c9a2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c9a2-113">-DefaultProfile</span></span>
<span data-ttu-id="7c9a2-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7c9a2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c9a2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7c9a2-115">-Force</span></span>
<span data-ttu-id="7c9a2-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="7c9a2-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7c9a2-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="7c9a2-117">-Name</span></span>
<span data-ttu-id="7c9a2-118">Especifica o nome de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="7c9a2-118">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="7c9a2-119">-ProtectedSettingFilePath</span><span class="sxs-lookup"><span data-stu-id="7c9a2-119">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="7c9a2-120">Especifica o caminho do arquivo de configuração particular.</span><span class="sxs-lookup"><span data-stu-id="7c9a2-120">Specifies the path of the private configuration file.</span></span>

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

### <span data-ttu-id="7c9a2-121">-SettingFilePath</span><span class="sxs-lookup"><span data-stu-id="7c9a2-121">-SettingFilePath</span></span>
<span data-ttu-id="7c9a2-122">Especifica o caminho do arquivo de configuração pública.</span><span class="sxs-lookup"><span data-stu-id="7c9a2-122">Specifies the path of the public configuration file.</span></span>

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

### <span data-ttu-id="7c9a2-123">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="7c9a2-123">-TypeHandlerVersion</span></span>
<span data-ttu-id="7c9a2-124">Especifica a versão da extensão a ser usada para este VMSS.</span><span class="sxs-lookup"><span data-stu-id="7c9a2-124">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="7c9a2-125">Para obter a versão, execute o cmdlet [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) com um valor de Microsoft. Azure. Diagnostics para o parâmetro *PublisherName* e IaaSDiagnostics para o parâmetro de *tipo* .</span><span class="sxs-lookup"><span data-stu-id="7c9a2-125">To obtain the version, run the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

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

### <span data-ttu-id="7c9a2-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7c9a2-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="7c9a2-127">Especifique o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="7c9a2-127">Specify the VMSS object.</span></span>
<span data-ttu-id="7c9a2-128">Você pode usar o cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="7c9a2-128">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="7c9a2-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7c9a2-129">-Confirm</span></span>
<span data-ttu-id="7c9a2-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c9a2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c9a2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c9a2-131">-WhatIf</span></span>
<span data-ttu-id="7c9a2-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7c9a2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c9a2-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7c9a2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c9a2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c9a2-134">CommonParameters</span></span>
<span data-ttu-id="7c9a2-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c9a2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c9a2-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c9a2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c9a2-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7c9a2-137">INPUTS</span></span>

### <span data-ttu-id="7c9a2-138">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7c9a2-138">VirtualMachineScaleSet</span></span>
<span data-ttu-id="7c9a2-139">O parâmetro ' VirtualMachineScaleSet ' aceita o valor do tipo ' VirtualMachineScaleSet ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="7c9a2-139">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="7c9a2-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7c9a2-140">OUTPUTS</span></span>

###  
<span data-ttu-id="7c9a2-141">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="7c9a2-141">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="7c9a2-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7c9a2-142">NOTES</span></span>

## <span data-ttu-id="7c9a2-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7c9a2-143">RELATED LINKS</span></span>

[<span data-ttu-id="7c9a2-144">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="7c9a2-144">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="7c9a2-145">Remove-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="7c9a2-145">Remove-AzureRmVmssDiagnosticsExtension</span></span>](./Remove-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="7c9a2-146">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="7c9a2-146">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)
