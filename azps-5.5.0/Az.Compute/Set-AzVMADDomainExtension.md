---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
ms.openlocfilehash: 1ea90503c1d022aa5a1925fa489e2ee63f4560ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127077"
---
# <span data-ttu-id="6831c-101">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="6831c-101">Set-AzVMADDomainExtension</span></span>

## <span data-ttu-id="6831c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6831c-102">SYNOPSIS</span></span>
<span data-ttu-id="6831c-103">Adiciona uma extensão de domínio AD a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6831c-103">Adds an AD domain extension to a virtual machine.</span></span>

## <span data-ttu-id="6831c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6831c-104">SYNTAX</span></span>

```
Set-AzVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6831c-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="6831c-105">DESCRIPTION</span></span>
<span data-ttu-id="6831c-106">O cmdlet **Set-AzVMADDomainExtension** adiciona uma extensão de máquina virtual de domínio do Azure Active Directory (AD) a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6831c-106">The **Set-AzVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="6831c-107">Essa extensão permite que sua máquina virtual in join a um domínio.</span><span class="sxs-lookup"><span data-stu-id="6831c-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="6831c-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6831c-108">EXAMPLES</span></span>

## <span data-ttu-id="6831c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6831c-109">PARAMETERS</span></span>

### <span data-ttu-id="6831c-110">-Credencial</span><span class="sxs-lookup"><span data-stu-id="6831c-110">-Credential</span></span>
<span data-ttu-id="6831c-111">Especifica o nome de usuário e a senha da máquina virtual como um **objeto PSCredential.**</span><span class="sxs-lookup"><span data-stu-id="6831c-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="6831c-112">Para obter uma credencial, use o Get-Credential cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6831c-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="6831c-113">Para obter mais informações, digite `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="6831c-113">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="6831c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6831c-114">-DefaultProfile</span></span>
<span data-ttu-id="6831c-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="6831c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6831c-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="6831c-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="6831c-117">Indica que esse cmdlet desabilita a atualização automática da versão secundária da extensão.</span><span class="sxs-lookup"><span data-stu-id="6831c-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="6831c-118">-DomainName</span><span class="sxs-lookup"><span data-stu-id="6831c-118">-DomainName</span></span>
<span data-ttu-id="6831c-119">Especifica o nome do domínio.</span><span class="sxs-lookup"><span data-stu-id="6831c-119">Specifies the name of the domain.</span></span>

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

### <span data-ttu-id="6831c-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="6831c-120">-ForceRerun</span></span>
<span data-ttu-id="6831c-121">Indica que esse cmdlet força uma nova execução da mesma configuração de extensão na máquina virtual sem desinstalar e reinstalar a extensão.</span><span class="sxs-lookup"><span data-stu-id="6831c-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="6831c-122">O valor pode ser qualquer cadeia de caracteres diferente do valor atual.</span><span class="sxs-lookup"><span data-stu-id="6831c-122">The value can be any string different from the current value.</span></span>
<span data-ttu-id="6831c-123">Se forceUpdateTag não for alterado, as atualizações para configurações públicas ou protegidas ainda serão aplicadas pelo manipulador.</span><span class="sxs-lookup"><span data-stu-id="6831c-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="6831c-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="6831c-124">-JoinOption</span></span>
<span data-ttu-id="6831c-125">Especifica a opção de junção.</span><span class="sxs-lookup"><span data-stu-id="6831c-125">Specifies the join option.</span></span> <span data-ttu-id="6831c-126">Para ver as opções de [junção, consulte fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span><span class="sxs-lookup"><span data-stu-id="6831c-126">For join options see [fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span></span>

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

### <span data-ttu-id="6831c-127">-Local</span><span class="sxs-lookup"><span data-stu-id="6831c-127">-Location</span></span>
<span data-ttu-id="6831c-128">Especifica a localização da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6831c-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="6831c-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="6831c-129">-Name</span></span>
<span data-ttu-id="6831c-130">Especifica o nome da extensão de domínio a ser acrescentada.</span><span class="sxs-lookup"><span data-stu-id="6831c-130">Specifies the name of the domain extension to add.</span></span>

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

### <span data-ttu-id="6831c-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6831c-131">-NoWait</span></span>
<span data-ttu-id="6831c-132">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="6831c-132">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="6831c-133">Para determinar se a operação foi concluída com êxito, use algum outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="6831c-133">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="6831c-134">-OUPath</span><span class="sxs-lookup"><span data-stu-id="6831c-134">-OUPath</span></span>
<span data-ttu-id="6831c-135">Especifica uma unidade organizacional (OU) para a conta de domínio.</span><span class="sxs-lookup"><span data-stu-id="6831c-135">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="6831c-136">Insira o nome completo diferenciado da UO entre aspas.</span><span class="sxs-lookup"><span data-stu-id="6831c-136">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="6831c-137">O valor padrão é o OU padrão para objetos de máquina no domínio.</span><span class="sxs-lookup"><span data-stu-id="6831c-137">The default value is the default OU for machine objects in the domain.</span></span>

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

### <span data-ttu-id="6831c-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6831c-138">-ResourceGroupName</span></span>
<span data-ttu-id="6831c-139">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6831c-139">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="6831c-140">-Reiniciar</span><span class="sxs-lookup"><span data-stu-id="6831c-140">-Restart</span></span>
<span data-ttu-id="6831c-141">Indica que esse cmdlet reinicia a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6831c-141">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="6831c-142">Muitas vezes, uma reinicialização é necessária para que a alteração seja efetivada.</span><span class="sxs-lookup"><span data-stu-id="6831c-142">A restart is often required to make the change effective.</span></span>

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

### <span data-ttu-id="6831c-143">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="6831c-143">-TypeHandlerVersion</span></span>
<span data-ttu-id="6831c-144">Especifica a versão da extensão de domínio.</span><span class="sxs-lookup"><span data-stu-id="6831c-144">Specifies the version of the domain extension.</span></span>

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

### <span data-ttu-id="6831c-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="6831c-145">-VMName</span></span>
<span data-ttu-id="6831c-146">Especifica o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6831c-146">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="6831c-147">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="6831c-147">-Confirm</span></span>
<span data-ttu-id="6831c-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6831c-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6831c-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6831c-149">-WhatIf</span></span>
<span data-ttu-id="6831c-150">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="6831c-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6831c-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6831c-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6831c-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6831c-152">CommonParameters</span></span>
<span data-ttu-id="6831c-153">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6831c-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6831c-154">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6831c-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6831c-155">Entradas</span><span class="sxs-lookup"><span data-stu-id="6831c-155">INPUTS</span></span>

### <span data-ttu-id="6831c-156">System.String</span><span class="sxs-lookup"><span data-stu-id="6831c-156">System.String</span></span>

### <span data-ttu-id="6831c-157">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6831c-157">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6831c-158">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="6831c-158">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="6831c-159">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6831c-159">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6831c-160">Saídas</span><span class="sxs-lookup"><span data-stu-id="6831c-160">OUTPUTS</span></span>

### <span data-ttu-id="6831c-161">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="6831c-161">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="6831c-162">Notas</span><span class="sxs-lookup"><span data-stu-id="6831c-162">NOTES</span></span>

## <span data-ttu-id="6831c-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6831c-163">RELATED LINKS</span></span>

[<span data-ttu-id="6831c-164">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="6831c-164">Get-AzVMADDomainExtension</span></span>](./Get-AzVMADDomainExtension.md)
