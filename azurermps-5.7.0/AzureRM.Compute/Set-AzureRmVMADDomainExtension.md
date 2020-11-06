---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
ms.openlocfilehash: b0af0f205f26862c20dd50e6181d2c11cd050dd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426780"
---
# <span data-ttu-id="dcd2e-101">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="dcd2e-101">Set-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="dcd2e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dcd2e-102">SYNOPSIS</span></span>
<span data-ttu-id="dcd2e-103">Adiciona uma extensão de domínio do AD a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dcd2e-103">Adds an AD domain extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcd2e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dcd2e-104">SYNTAX</span></span>

```
Set-AzureRmVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcd2e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dcd2e-105">DESCRIPTION</span></span>
<span data-ttu-id="dcd2e-106">O cmdlet **set-AzureRmVMADDomainExtension** adiciona uma extensão de máquina virtual de domínio do Azure Active Directory (AD) a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dcd2e-106">The **Set-AzureRmVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="dcd2e-107">Esta extensão permite que a máquina virtual ingresse em um domínio.</span><span class="sxs-lookup"><span data-stu-id="dcd2e-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="dcd2e-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dcd2e-108">EXAMPLES</span></span>

## <span data-ttu-id="dcd2e-109">OS</span><span class="sxs-lookup"><span data-stu-id="dcd2e-109">PARAMETERS</span></span>

### <span data-ttu-id="dcd2e-110">-Credential</span><span class="sxs-lookup"><span data-stu-id="dcd2e-110">-Credential</span></span>
<span data-ttu-id="dcd2e-111">Especifica o nome de usuário e a senha da máquina virtual como um objeto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="dcd2e-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="dcd2e-112">Para obter uma credencial, use o cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="dcd2e-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="dcd2e-113">Para obter mais informações, digite `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="dcd2e-113">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd2e-114">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="dcd2e-114">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="dcd2e-115">Indica que esse cmdlet desabilita a atualização automática da versão secundária da extensão.</span><span class="sxs-lookup"><span data-stu-id="dcd2e-115">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd2e-116">-DomainName</span><span class="sxs-lookup"><span data-stu-id="dcd2e-116">-DomainName</span></span>
<span data-ttu-id="dcd2e-117">Especifica o nome do domínio.</span><span class="sxs-lookup"><span data-stu-id="dcd2e-117">Specifies the name of the domain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd2e-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="dcd2e-118">-ForceRerun</span></span>
<span data-ttu-id="dcd2e-119">Indica que esse cmdlet força uma nova configuração da mesma extensão na máquina virtual sem desinstalar e reinstalar a extensão.</span><span class="sxs-lookup"><span data-stu-id="dcd2e-119">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="dcd2e-120">O valor pode ser qualquer cadeia de caracteres diferente do valor atual.</span><span class="sxs-lookup"><span data-stu-id="dcd2e-120">The value can be any string different from the current value.</span></span>

<span data-ttu-id="dcd2e-121">Se forceUpdateTag não for alterado, as atualizações para as configurações públicas ou protegidas ainda serão aplicadas pelo manipulador.</span><span class="sxs-lookup"><span data-stu-id="dcd2e-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd2e-122">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="dcd2e-122">-JoinOption</span></span>
<span data-ttu-id="dcd2e-123">Especifica a opção de junção.</span><span class="sxs-lookup"><span data-stu-id="dcd2e-123">Specifies the join option.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd2e-124">-Local</span><span class="sxs-lookup"><span data-stu-id="dcd2e-124">-Location</span></span>
<span data-ttu-id="dcd2e-125">Especifica o local da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dcd2e-125">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd2e-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="dcd2e-126">-Name</span></span>
<span data-ttu-id="dcd2e-127">Especifica o nome da extensão de domínio a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="dcd2e-127">Specifies the name of the domain extension to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd2e-128">-OUPath</span><span class="sxs-lookup"><span data-stu-id="dcd2e-128">-OUPath</span></span>
<span data-ttu-id="dcd2e-129">Especifica uma unidade organizacional (OU) para a conta de domínio.</span><span class="sxs-lookup"><span data-stu-id="dcd2e-129">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="dcd2e-130">Digite o nome diferenciado completo da UO entre aspas.</span><span class="sxs-lookup"><span data-stu-id="dcd2e-130">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="dcd2e-131">O valor padrão é a UO padrão para objetos de máquina no domínio.</span><span class="sxs-lookup"><span data-stu-id="dcd2e-131">The default value is the default OU for machine objects in the domain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd2e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcd2e-132">-ResourceGroupName</span></span>
<span data-ttu-id="dcd2e-133">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dcd2e-133">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd2e-134">-Restart</span><span class="sxs-lookup"><span data-stu-id="dcd2e-134">-Restart</span></span>
<span data-ttu-id="dcd2e-135">Indica que esse cmdlet reinicia a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dcd2e-135">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="dcd2e-136">Uma reinicialização geralmente é necessária para fazer a mudança entrar em vigor.</span><span class="sxs-lookup"><span data-stu-id="dcd2e-136">A restart is often required to make the change effective.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd2e-137">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="dcd2e-137">-TypeHandlerVersion</span></span>
<span data-ttu-id="dcd2e-138">Especifica a versão da extensão do domínio.</span><span class="sxs-lookup"><span data-stu-id="dcd2e-138">Specifies the version of the domain extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd2e-139">-VMName</span><span class="sxs-lookup"><span data-stu-id="dcd2e-139">-VMName</span></span>
<span data-ttu-id="dcd2e-140">Especifica o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dcd2e-140">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd2e-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dcd2e-141">-Confirm</span></span>
<span data-ttu-id="dcd2e-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcd2e-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcd2e-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcd2e-143">-WhatIf</span></span>
<span data-ttu-id="dcd2e-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dcd2e-144">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="dcd2e-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dcd2e-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcd2e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcd2e-146">CommonParameters</span></span>
<span data-ttu-id="dcd2e-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcd2e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcd2e-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcd2e-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcd2e-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dcd2e-149">INPUTS</span></span>

### <span data-ttu-id="dcd2e-150">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="dcd2e-150">None</span></span>
<span data-ttu-id="dcd2e-151">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="dcd2e-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dcd2e-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dcd2e-152">OUTPUTS</span></span>

## <span data-ttu-id="dcd2e-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dcd2e-153">NOTES</span></span>

## <span data-ttu-id="dcd2e-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dcd2e-154">RELATED LINKS</span></span>

[<span data-ttu-id="dcd2e-155">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="dcd2e-155">Get-AzureRmVMADDomainExtension</span></span>](./Get-AzureRmVMADDomainExtension.md)
