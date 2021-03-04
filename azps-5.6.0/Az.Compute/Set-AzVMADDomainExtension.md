---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
ms.openlocfilehash: 03f898246b2f0d784725488f753697ed893b09df
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901501"
---
# <span data-ttu-id="87ad5-101">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="87ad5-101">Set-AzVMADDomainExtension</span></span>

## <span data-ttu-id="87ad5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87ad5-102">SYNOPSIS</span></span>
<span data-ttu-id="87ad5-103">Adiciona uma extensão de domínio do AD a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="87ad5-103">Adds an AD domain extension to a virtual machine.</span></span>

## <span data-ttu-id="87ad5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="87ad5-104">SYNTAX</span></span>

```
Set-AzVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87ad5-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="87ad5-105">DESCRIPTION</span></span>
<span data-ttu-id="87ad5-106">O cmdlet **Set-AzVMADDomainExtension** adiciona uma extensão de máquina virtual de domínio do Azure Active Directory (AD) a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="87ad5-106">The **Set-AzVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="87ad5-107">Essa extensão permite que sua máquina virtual participe de um domínio.</span><span class="sxs-lookup"><span data-stu-id="87ad5-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="87ad5-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="87ad5-108">EXAMPLES</span></span>

## <span data-ttu-id="87ad5-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="87ad5-109">PARAMETERS</span></span>

### <span data-ttu-id="87ad5-110">-Credential</span><span class="sxs-lookup"><span data-stu-id="87ad5-110">-Credential</span></span>
<span data-ttu-id="87ad5-111">Especifica o nome de usuário e a senha da máquina virtual como um **objeto PSCredential.**</span><span class="sxs-lookup"><span data-stu-id="87ad5-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="87ad5-112">Para obter uma credencial, use Get-Credential cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87ad5-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="87ad5-113">Para obter mais informações, digite `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="87ad5-113">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="87ad5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87ad5-114">-DefaultProfile</span></span>
<span data-ttu-id="87ad5-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="87ad5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87ad5-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="87ad5-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="87ad5-117">Indica que esse cmdlet desabilita a atualização automática da versão secundária da extensão.</span><span class="sxs-lookup"><span data-stu-id="87ad5-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="87ad5-118">-DomainName</span><span class="sxs-lookup"><span data-stu-id="87ad5-118">-DomainName</span></span>
<span data-ttu-id="87ad5-119">Especifica o nome do domínio.</span><span class="sxs-lookup"><span data-stu-id="87ad5-119">Specifies the name of the domain.</span></span>

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

### <span data-ttu-id="87ad5-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="87ad5-120">-ForceRerun</span></span>
<span data-ttu-id="87ad5-121">Indica que esse cmdlet força uma repetição da mesma configuração de extensão na máquina virtual sem desinstalar e reinstalar a extensão.</span><span class="sxs-lookup"><span data-stu-id="87ad5-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="87ad5-122">O valor pode ser qualquer cadeia de caracteres diferente do valor atual.</span><span class="sxs-lookup"><span data-stu-id="87ad5-122">The value can be any string different from the current value.</span></span>
<span data-ttu-id="87ad5-123">Se forceUpdateTag não for alterado, as atualizações para configurações públicas ou protegidas ainda serão aplicadas pelo manipulador.</span><span class="sxs-lookup"><span data-stu-id="87ad5-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="87ad5-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="87ad5-124">-JoinOption</span></span>
<span data-ttu-id="87ad5-125">Especifica a opção de junção.</span><span class="sxs-lookup"><span data-stu-id="87ad5-125">Specifies the join option.</span></span> <span data-ttu-id="87ad5-126">Para ver opções de [junção, consulte fJoinOptions](https://docs.microsoft.com/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span><span class="sxs-lookup"><span data-stu-id="87ad5-126">For join options see [fJoinOptions](https://docs.microsoft.com/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span></span>

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

### <span data-ttu-id="87ad5-127">-Location</span><span class="sxs-lookup"><span data-stu-id="87ad5-127">-Location</span></span>
<span data-ttu-id="87ad5-128">Especifica o local da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="87ad5-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="87ad5-129">-Name</span><span class="sxs-lookup"><span data-stu-id="87ad5-129">-Name</span></span>
<span data-ttu-id="87ad5-130">Especifica o nome da extensão de domínio a ser acrescentada.</span><span class="sxs-lookup"><span data-stu-id="87ad5-130">Specifies the name of the domain extension to add.</span></span>

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

### <span data-ttu-id="87ad5-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="87ad5-131">-NoWait</span></span>
<span data-ttu-id="87ad5-132">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="87ad5-132">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="87ad5-133">Para determinar se a operação foi concluída com êxito, use algum outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="87ad5-133">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87ad5-134">-OUPath</span><span class="sxs-lookup"><span data-stu-id="87ad5-134">-OUPath</span></span>
<span data-ttu-id="87ad5-135">Especifica uma unidade organizacional (UO) para a conta de domínio.</span><span class="sxs-lookup"><span data-stu-id="87ad5-135">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="87ad5-136">Insira o nome diferenciado completo da UO entre aspas.</span><span class="sxs-lookup"><span data-stu-id="87ad5-136">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="87ad5-137">O valor padrão é a UO padrão para objetos de máquina no domínio.</span><span class="sxs-lookup"><span data-stu-id="87ad5-137">The default value is the default OU for machine objects in the domain.</span></span>

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

### <span data-ttu-id="87ad5-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87ad5-138">-ResourceGroupName</span></span>
<span data-ttu-id="87ad5-139">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="87ad5-139">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="87ad5-140">-Restart</span><span class="sxs-lookup"><span data-stu-id="87ad5-140">-Restart</span></span>
<span data-ttu-id="87ad5-141">Indica que esse cmdlet reinicia a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="87ad5-141">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="87ad5-142">Geralmente, uma reinicialização é necessária para tornar a alteração efetiva.</span><span class="sxs-lookup"><span data-stu-id="87ad5-142">A restart is often required to make the change effective.</span></span>

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

### <span data-ttu-id="87ad5-143">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="87ad5-143">-TypeHandlerVersion</span></span>
<span data-ttu-id="87ad5-144">Especifica a versão da extensão de domínio.</span><span class="sxs-lookup"><span data-stu-id="87ad5-144">Specifies the version of the domain extension.</span></span>

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

### <span data-ttu-id="87ad5-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="87ad5-145">-VMName</span></span>
<span data-ttu-id="87ad5-146">Especifica o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="87ad5-146">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="87ad5-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="87ad5-147">-Confirm</span></span>
<span data-ttu-id="87ad5-148">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87ad5-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87ad5-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87ad5-149">-WhatIf</span></span>
<span data-ttu-id="87ad5-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="87ad5-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87ad5-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="87ad5-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87ad5-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87ad5-152">CommonParameters</span></span>
<span data-ttu-id="87ad5-153">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87ad5-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87ad5-154">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87ad5-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87ad5-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="87ad5-155">INPUTS</span></span>

### <span data-ttu-id="87ad5-156">System.String</span><span class="sxs-lookup"><span data-stu-id="87ad5-156">System.String</span></span>

### <span data-ttu-id="87ad5-157">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="87ad5-157">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="87ad5-158">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="87ad5-158">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="87ad5-159">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="87ad5-159">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="87ad5-160">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="87ad5-160">OUTPUTS</span></span>

### <span data-ttu-id="87ad5-161">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="87ad5-161">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="87ad5-162">NOTES</span><span class="sxs-lookup"><span data-stu-id="87ad5-162">NOTES</span></span>

## <span data-ttu-id="87ad5-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="87ad5-163">RELATED LINKS</span></span>

[<span data-ttu-id="87ad5-164">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="87ad5-164">Get-AzVMADDomainExtension</span></span>](./Get-AzVMADDomainExtension.md)
