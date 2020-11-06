---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAccessExtension.md
ms.openlocfilehash: c77fe7985e91386cad746c61f5849072e0366615
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426937"
---
# <span data-ttu-id="fe9f9-101">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="fe9f9-101">Set-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="fe9f9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fe9f9-102">SYNOPSIS</span></span>
<span data-ttu-id="fe9f9-103">Adiciona a extensão VMAccess a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fe9f9-103">Adds the VMAccess extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe9f9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fe9f9-104">SYNTAX</span></span>

```
Set-AzureRmVMAccessExtension [-UserName <String>] [-Password <String>] [-ResourceGroupName] <String>
 [-VMName] <String> [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe9f9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fe9f9-105">DESCRIPTION</span></span>
<span data-ttu-id="fe9f9-106">O cmdlet **set-AzureRmVMAccessExtension** adiciona a extensão da máquina virtual do VMAccess (acesso à máquina virtual) a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fe9f9-106">The **Set-AzureRmVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="fe9f9-107">VMAccess pode redefinir o nome de usuário e a senha da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fe9f9-107">VMAccess can reset the virtual machine user name and password.</span></span>

## <span data-ttu-id="fe9f9-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fe9f9-108">EXAMPLES</span></span>

### <span data-ttu-id="fe9f9-109">Exemplo 1: adicionar uma extensão VMAccess</span><span class="sxs-lookup"><span data-stu-id="fe9f9-109">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzureRmVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.0" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="fe9f9-110">Esse comando adiciona uma extensão VMAccess para a máquina virtual nomeada VirtualMachine07 no ResrouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="fe9f9-110">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResrouceGroup11.</span></span>
<span data-ttu-id="fe9f9-111">O comando especifica o nome e a versão do manipulador de tipo para VMAccess.</span><span class="sxs-lookup"><span data-stu-id="fe9f9-111">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="fe9f9-112">OS</span><span class="sxs-lookup"><span data-stu-id="fe9f9-112">PARAMETERS</span></span>

### <span data-ttu-id="fe9f9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe9f9-113">-DefaultProfile</span></span>
<span data-ttu-id="fe9f9-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fe9f9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe9f9-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="fe9f9-115">-DisableAutoUpgradeMinorVersion</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe9f9-116">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="fe9f9-116">-ForceRerun</span></span>
<span data-ttu-id="fe9f9-117">Indica que esse cmdlet força uma nova configuração da mesma extensão na máquina virtual sem desinstalar e reinstalar a extensão.</span><span class="sxs-lookup"><span data-stu-id="fe9f9-117">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="fe9f9-118">O valor pode ser qualquer cadeia de caracteres diferente do valor atual.</span><span class="sxs-lookup"><span data-stu-id="fe9f9-118">The value can be any string different from the current value.</span></span>

<span data-ttu-id="fe9f9-119">Se forceUpdateTag não for alterado, as atualizações para as configurações públicas ou protegidas ainda serão aplicadas pelo manipulador.</span><span class="sxs-lookup"><span data-stu-id="fe9f9-119">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe9f9-120">-Local</span><span class="sxs-lookup"><span data-stu-id="fe9f9-120">-Location</span></span>
<span data-ttu-id="fe9f9-121">Especifica o local da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fe9f9-121">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe9f9-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="fe9f9-122">-Name</span></span>
<span data-ttu-id="fe9f9-123">Especifica o nome da extensão que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="fe9f9-123">Specifies the name of the extension that this cmdlet adds.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe9f9-124">-Senha</span><span class="sxs-lookup"><span data-stu-id="fe9f9-124">-Password</span></span>
<span data-ttu-id="fe9f9-125">Especifica a nova senha da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fe9f9-125">Specifies the new password of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe9f9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe9f9-126">-ResourceGroupName</span></span>
<span data-ttu-id="fe9f9-127">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fe9f9-127">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe9f9-128">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="fe9f9-128">-TypeHandlerVersion</span></span>
<span data-ttu-id="fe9f9-129">Especifica a versão da extensão a ser usada para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fe9f9-129">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="fe9f9-130">Para obter a versão, execute o cmdlet Get-AzureRmVMExtensionImage com um valor de Microsoft. COMPUTE para o parâmetro *PublisherName* e VMAccessAgent para o parâmetro de *tipo* .</span><span class="sxs-lookup"><span data-stu-id="fe9f9-130">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe9f9-131">-UserName</span><span class="sxs-lookup"><span data-stu-id="fe9f9-131">-UserName</span></span>
<span data-ttu-id="fe9f9-132">Especifica o novo nome de usuário para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fe9f9-132">Specifies the new user name for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe9f9-133">-VMName</span><span class="sxs-lookup"><span data-stu-id="fe9f9-133">-VMName</span></span>
<span data-ttu-id="fe9f9-134">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fe9f9-134">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="fe9f9-135">Esse cmdlet adiciona VMAccess para a máquina virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="fe9f9-135">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe9f9-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fe9f9-136">-Confirm</span></span>
<span data-ttu-id="fe9f9-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe9f9-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9f9-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe9f9-138">-WhatIf</span></span>
<span data-ttu-id="fe9f9-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fe9f9-139">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="fe9f9-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fe9f9-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9f9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe9f9-141">CommonParameters</span></span>
<span data-ttu-id="fe9f9-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe9f9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe9f9-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe9f9-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe9f9-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fe9f9-144">INPUTS</span></span>

## <span data-ttu-id="fe9f9-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fe9f9-145">OUTPUTS</span></span>

## <span data-ttu-id="fe9f9-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fe9f9-146">NOTES</span></span>

## <span data-ttu-id="fe9f9-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fe9f9-147">RELATED LINKS</span></span>

[<span data-ttu-id="fe9f9-148">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="fe9f9-148">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="fe9f9-149">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="fe9f9-149">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="fe9f9-150">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="fe9f9-150">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)

[<span data-ttu-id="fe9f9-151">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="fe9f9-151">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)


