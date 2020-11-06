---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
ms.openlocfilehash: 5b590bf882acc373b4219069f8feff4c5060cf59
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601241"
---
# <span data-ttu-id="1c6b3-101">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="1c6b3-101">Set-AzVMADDomainExtension</span></span>

## <span data-ttu-id="1c6b3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1c6b3-102">SYNOPSIS</span></span>
<span data-ttu-id="1c6b3-103">Adiciona uma extensão de domínio do AD a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-103">Adds an AD domain extension to a virtual machine.</span></span>

## <span data-ttu-id="1c6b3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1c6b3-104">SYNTAX</span></span>

```
Set-AzVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c6b3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1c6b3-105">DESCRIPTION</span></span>
<span data-ttu-id="1c6b3-106">O cmdlet **set-AzVMADDomainExtension** adiciona uma extensão de máquina virtual de domínio do Azure Active Directory (AD) a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-106">The **Set-AzVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="1c6b3-107">Esta extensão permite que a máquina virtual ingresse em um domínio.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="1c6b3-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1c6b3-108">EXAMPLES</span></span>

## <span data-ttu-id="1c6b3-109">OS</span><span class="sxs-lookup"><span data-stu-id="1c6b3-109">PARAMETERS</span></span>

### <span data-ttu-id="1c6b3-110">-Credential</span><span class="sxs-lookup"><span data-stu-id="1c6b3-110">-Credential</span></span>
<span data-ttu-id="1c6b3-111">Especifica o nome de usuário e a senha da máquina virtual como um objeto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="1c6b3-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="1c6b3-112">Para obter uma credencial, use o cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="1c6b3-113">Para obter mais informações, digite `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="1c6b3-113">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c6b3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c6b3-114">-DefaultProfile</span></span>
<span data-ttu-id="1c6b3-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c6b3-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="1c6b3-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="1c6b3-117">Indica que esse cmdlet desabilita a atualização automática da versão secundária da extensão.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="1c6b3-118">-DomainName</span><span class="sxs-lookup"><span data-stu-id="1c6b3-118">-DomainName</span></span>
<span data-ttu-id="1c6b3-119">Especifica o nome do domínio.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-119">Specifies the name of the domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c6b3-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="1c6b3-120">-ForceRerun</span></span>
<span data-ttu-id="1c6b3-121">Indica que esse cmdlet força uma nova configuração da mesma extensão na máquina virtual sem desinstalar e reinstalar a extensão.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="1c6b3-122">O valor pode ser qualquer cadeia de caracteres diferente do valor atual.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-122">The value can be any string different from the current value.</span></span>
<span data-ttu-id="1c6b3-123">Se forceUpdateTag não for alterado, as atualizações para as configurações públicas ou protegidas ainda serão aplicadas pelo manipulador.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="1c6b3-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="1c6b3-124">-JoinOption</span></span>
<span data-ttu-id="1c6b3-125">Especifica a opção de junção.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-125">Specifies the join option.</span></span> <span data-ttu-id="1c6b3-126">Para opções de junção, consulte [fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span><span class="sxs-lookup"><span data-stu-id="1c6b3-126">For join options see [fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c6b3-127">-Local</span><span class="sxs-lookup"><span data-stu-id="1c6b3-127">-Location</span></span>
<span data-ttu-id="1c6b3-128">Especifica o local da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="1c6b3-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="1c6b3-129">-Name</span></span>
<span data-ttu-id="1c6b3-130">Especifica o nome da extensão de domínio a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-130">Specifies the name of the domain extension to add.</span></span>

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

### <span data-ttu-id="1c6b3-131">-OUPath</span><span class="sxs-lookup"><span data-stu-id="1c6b3-131">-OUPath</span></span>
<span data-ttu-id="1c6b3-132">Especifica uma unidade organizacional (OU) para a conta de domínio.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-132">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="1c6b3-133">Digite o nome diferenciado completo da UO entre aspas.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-133">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="1c6b3-134">O valor padrão é a UO padrão para objetos de máquina no domínio.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-134">The default value is the default OU for machine objects in the domain.</span></span>

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

### <span data-ttu-id="1c6b3-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c6b3-135">-ResourceGroupName</span></span>
<span data-ttu-id="1c6b3-136">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-136">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="1c6b3-137">-Restart</span><span class="sxs-lookup"><span data-stu-id="1c6b3-137">-Restart</span></span>
<span data-ttu-id="1c6b3-138">Indica que esse cmdlet reinicia a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-138">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="1c6b3-139">Uma reinicialização geralmente é necessária para fazer a mudança entrar em vigor.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-139">A restart is often required to make the change effective.</span></span>

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

### <span data-ttu-id="1c6b3-140">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="1c6b3-140">-TypeHandlerVersion</span></span>
<span data-ttu-id="1c6b3-141">Especifica a versão da extensão do domínio.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-141">Specifies the version of the domain extension.</span></span>

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

### <span data-ttu-id="1c6b3-142">-VMName</span><span class="sxs-lookup"><span data-stu-id="1c6b3-142">-VMName</span></span>
<span data-ttu-id="1c6b3-143">Especifica o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-143">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="1c6b3-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1c6b3-144">-Confirm</span></span>
<span data-ttu-id="1c6b3-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c6b3-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c6b3-146">-WhatIf</span></span>
<span data-ttu-id="1c6b3-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c6b3-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c6b3-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c6b3-149">CommonParameters</span></span>
<span data-ttu-id="1c6b3-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c6b3-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c6b3-151">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c6b3-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c6b3-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1c6b3-152">INPUTS</span></span>

### <span data-ttu-id="1c6b3-153">System. String</span><span class="sxs-lookup"><span data-stu-id="1c6b3-153">System.String</span></span>

### <span data-ttu-id="1c6b3-154">System. Nullable ' 1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1c6b3-154">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1c6b3-155">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="1c6b3-155">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="1c6b3-156">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1c6b3-156">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1c6b3-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1c6b3-157">OUTPUTS</span></span>

### <span data-ttu-id="1c6b3-158">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1c6b3-158">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1c6b3-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1c6b3-159">NOTES</span></span>

## <span data-ttu-id="1c6b3-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1c6b3-160">RELATED LINKS</span></span>

[<span data-ttu-id="1c6b3-161">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="1c6b3-161">Get-AzVMADDomainExtension</span></span>](./Get-AzVMADDomainExtension.md)
