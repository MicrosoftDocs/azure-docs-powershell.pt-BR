---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
ms.openlocfilehash: 99dd311adf976e100282da92db6a3147880feefb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776849"
---
# <span data-ttu-id="e1ba4-101">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="e1ba4-101">Set-AzVMADDomainExtension</span></span>

## <span data-ttu-id="e1ba4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e1ba4-102">SYNOPSIS</span></span>
<span data-ttu-id="e1ba4-103">Adiciona uma extensão de domínio do AD a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e1ba4-103">Adds an AD domain extension to a virtual machine.</span></span>

## <span data-ttu-id="e1ba4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e1ba4-104">SYNTAX</span></span>

```
Set-AzVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1ba4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e1ba4-105">DESCRIPTION</span></span>
<span data-ttu-id="e1ba4-106">O cmdlet **set-AzVMADDomainExtension** adiciona uma extensão de máquina virtual de domínio do Azure Active Directory (AD) a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e1ba4-106">The **Set-AzVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="e1ba4-107">Esta extensão permite que a máquina virtual ingresse em um domínio.</span><span class="sxs-lookup"><span data-stu-id="e1ba4-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="e1ba4-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e1ba4-108">EXAMPLES</span></span>

## <span data-ttu-id="e1ba4-109">OS</span><span class="sxs-lookup"><span data-stu-id="e1ba4-109">PARAMETERS</span></span>

### <span data-ttu-id="e1ba4-110">-Credential</span><span class="sxs-lookup"><span data-stu-id="e1ba4-110">-Credential</span></span>
<span data-ttu-id="e1ba4-111">Especifica o nome de usuário e a senha da máquina virtual como um objeto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="e1ba4-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="e1ba4-112">Para obter uma credencial, use o cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="e1ba4-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="e1ba4-113">Para obter mais informações, digite `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="e1ba4-113">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="e1ba4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1ba4-114">-DefaultProfile</span></span>
<span data-ttu-id="e1ba4-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e1ba4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1ba4-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="e1ba4-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="e1ba4-117">Indica que esse cmdlet desabilita a atualização automática da versão secundária da extensão.</span><span class="sxs-lookup"><span data-stu-id="e1ba4-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="e1ba4-118">-DomainName</span><span class="sxs-lookup"><span data-stu-id="e1ba4-118">-DomainName</span></span>
<span data-ttu-id="e1ba4-119">Especifica o nome do domínio.</span><span class="sxs-lookup"><span data-stu-id="e1ba4-119">Specifies the name of the domain.</span></span>

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

### <span data-ttu-id="e1ba4-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="e1ba4-120">-ForceRerun</span></span>
<span data-ttu-id="e1ba4-121">Indica que esse cmdlet força uma nova configuração da mesma extensão na máquina virtual sem desinstalar e reinstalar a extensão.</span><span class="sxs-lookup"><span data-stu-id="e1ba4-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="e1ba4-122">O valor pode ser qualquer cadeia de caracteres diferente do valor atual.</span><span class="sxs-lookup"><span data-stu-id="e1ba4-122">The value can be any string different from the current value.</span></span>

<span data-ttu-id="e1ba4-123">Se forceUpdateTag não for alterado, as atualizações para as configurações públicas ou protegidas ainda serão aplicadas pelo manipulador.</span><span class="sxs-lookup"><span data-stu-id="e1ba4-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="e1ba4-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="e1ba4-124">-JoinOption</span></span>
<span data-ttu-id="e1ba4-125">Especifica a opção de junção.</span><span class="sxs-lookup"><span data-stu-id="e1ba4-125">Specifies the join option.</span></span>

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

### <span data-ttu-id="e1ba4-126">-Local</span><span class="sxs-lookup"><span data-stu-id="e1ba4-126">-Location</span></span>
<span data-ttu-id="e1ba4-127">Especifica o local da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e1ba4-127">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="e1ba4-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="e1ba4-128">-Name</span></span>
<span data-ttu-id="e1ba4-129">Especifica o nome da extensão de domínio a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="e1ba4-129">Specifies the name of the domain extension to add.</span></span>

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

### <span data-ttu-id="e1ba4-130">-OUPath</span><span class="sxs-lookup"><span data-stu-id="e1ba4-130">-OUPath</span></span>
<span data-ttu-id="e1ba4-131">Especifica uma unidade organizacional (OU) para a conta de domínio.</span><span class="sxs-lookup"><span data-stu-id="e1ba4-131">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="e1ba4-132">Digite o nome diferenciado completo da UO entre aspas.</span><span class="sxs-lookup"><span data-stu-id="e1ba4-132">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="e1ba4-133">O valor padrão é a UO padrão para objetos de máquina no domínio.</span><span class="sxs-lookup"><span data-stu-id="e1ba4-133">The default value is the default OU for machine objects in the domain.</span></span>

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

### <span data-ttu-id="e1ba4-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1ba4-134">-ResourceGroupName</span></span>
<span data-ttu-id="e1ba4-135">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e1ba4-135">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e1ba4-136">-Restart</span><span class="sxs-lookup"><span data-stu-id="e1ba4-136">-Restart</span></span>
<span data-ttu-id="e1ba4-137">Indica que esse cmdlet reinicia a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e1ba4-137">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="e1ba4-138">Uma reinicialização geralmente é necessária para fazer a mudança entrar em vigor.</span><span class="sxs-lookup"><span data-stu-id="e1ba4-138">A restart is often required to make the change effective.</span></span>

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

### <span data-ttu-id="e1ba4-139">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="e1ba4-139">-TypeHandlerVersion</span></span>
<span data-ttu-id="e1ba4-140">Especifica a versão da extensão do domínio.</span><span class="sxs-lookup"><span data-stu-id="e1ba4-140">Specifies the version of the domain extension.</span></span>

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

### <span data-ttu-id="e1ba4-141">-VMName</span><span class="sxs-lookup"><span data-stu-id="e1ba4-141">-VMName</span></span>
<span data-ttu-id="e1ba4-142">Especifica o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e1ba4-142">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="e1ba4-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e1ba4-143">-Confirm</span></span>
<span data-ttu-id="e1ba4-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1ba4-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1ba4-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1ba4-145">-WhatIf</span></span>
<span data-ttu-id="e1ba4-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e1ba4-146">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="e1ba4-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e1ba4-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1ba4-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1ba4-148">CommonParameters</span></span>
<span data-ttu-id="e1ba4-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1ba4-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1ba4-150">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1ba4-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1ba4-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e1ba4-151">INPUTS</span></span>

### <span data-ttu-id="e1ba4-152">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e1ba4-152">None</span></span>
<span data-ttu-id="e1ba4-153">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="e1ba4-153">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e1ba4-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e1ba4-154">OUTPUTS</span></span>

### <span data-ttu-id="e1ba4-155">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e1ba4-155">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e1ba4-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e1ba4-156">NOTES</span></span>

## <span data-ttu-id="e1ba4-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e1ba4-157">RELATED LINKS</span></span>

[<span data-ttu-id="e1ba4-158">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="e1ba4-158">Get-AzVMADDomainExtension</span></span>](./Get-AzVMADDomainExtension.md)
