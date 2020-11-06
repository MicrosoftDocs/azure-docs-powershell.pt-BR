---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
ms.openlocfilehash: 663363ae2da1c17a9797f25260fa5a0b891fa483
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602062"
---
# <span data-ttu-id="b8dbd-101">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="b8dbd-101">Set-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="b8dbd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b8dbd-102">SYNOPSIS</span></span>
<span data-ttu-id="b8dbd-103">Adiciona uma extensão de domínio do AD a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b8dbd-103">Adds an AD domain extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8dbd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8dbd-104">SYNTAX</span></span>

```
Set-AzureRmVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8dbd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b8dbd-105">DESCRIPTION</span></span>
<span data-ttu-id="b8dbd-106">O cmdlet **set-AzureRmVMADDomainExtension** adiciona uma extensão de máquina virtual de domínio do Azure Active Directory (AD) a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b8dbd-106">The **Set-AzureRmVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="b8dbd-107">Esta extensão permite que a máquina virtual ingresse em um domínio.</span><span class="sxs-lookup"><span data-stu-id="b8dbd-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="b8dbd-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b8dbd-108">EXAMPLES</span></span>

## <span data-ttu-id="b8dbd-109">OS</span><span class="sxs-lookup"><span data-stu-id="b8dbd-109">PARAMETERS</span></span>

### <span data-ttu-id="b8dbd-110">-Credential</span><span class="sxs-lookup"><span data-stu-id="b8dbd-110">-Credential</span></span>
<span data-ttu-id="b8dbd-111">Especifica o nome de usuário e a senha da máquina virtual como um objeto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="b8dbd-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="b8dbd-112">Para obter uma credencial, use o cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="b8dbd-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="b8dbd-113">Para obter mais informações, digite `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="b8dbd-113">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="b8dbd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8dbd-114">-DefaultProfile</span></span>
<span data-ttu-id="b8dbd-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b8dbd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8dbd-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="b8dbd-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="b8dbd-117">Indica que esse cmdlet desabilita a atualização automática da versão secundária da extensão.</span><span class="sxs-lookup"><span data-stu-id="b8dbd-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="b8dbd-118">-DomainName</span><span class="sxs-lookup"><span data-stu-id="b8dbd-118">-DomainName</span></span>
<span data-ttu-id="b8dbd-119">Especifica o nome do domínio.</span><span class="sxs-lookup"><span data-stu-id="b8dbd-119">Specifies the name of the domain.</span></span>

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

### <span data-ttu-id="b8dbd-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="b8dbd-120">-ForceRerun</span></span>
<span data-ttu-id="b8dbd-121">Indica que esse cmdlet força uma nova configuração da mesma extensão na máquina virtual sem desinstalar e reinstalar a extensão.</span><span class="sxs-lookup"><span data-stu-id="b8dbd-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="b8dbd-122">O valor pode ser qualquer cadeia de caracteres diferente do valor atual.</span><span class="sxs-lookup"><span data-stu-id="b8dbd-122">The value can be any string different from the current value.</span></span>

<span data-ttu-id="b8dbd-123">Se forceUpdateTag não for alterado, as atualizações para as configurações públicas ou protegidas ainda serão aplicadas pelo manipulador.</span><span class="sxs-lookup"><span data-stu-id="b8dbd-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="b8dbd-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="b8dbd-124">-JoinOption</span></span>
<span data-ttu-id="b8dbd-125">Especifica a opção de junção.</span><span class="sxs-lookup"><span data-stu-id="b8dbd-125">Specifies the join option.</span></span>

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

### <span data-ttu-id="b8dbd-126">-Local</span><span class="sxs-lookup"><span data-stu-id="b8dbd-126">-Location</span></span>
<span data-ttu-id="b8dbd-127">Especifica o local da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b8dbd-127">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="b8dbd-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="b8dbd-128">-Name</span></span>
<span data-ttu-id="b8dbd-129">Especifica o nome da extensão de domínio a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="b8dbd-129">Specifies the name of the domain extension to add.</span></span>

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

### <span data-ttu-id="b8dbd-130">-OUPath</span><span class="sxs-lookup"><span data-stu-id="b8dbd-130">-OUPath</span></span>
<span data-ttu-id="b8dbd-131">Especifica uma unidade organizacional (OU) para a conta de domínio.</span><span class="sxs-lookup"><span data-stu-id="b8dbd-131">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="b8dbd-132">Digite o nome diferenciado completo da UO entre aspas.</span><span class="sxs-lookup"><span data-stu-id="b8dbd-132">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="b8dbd-133">O valor padrão é a UO padrão para objetos de máquina no domínio.</span><span class="sxs-lookup"><span data-stu-id="b8dbd-133">The default value is the default OU for machine objects in the domain.</span></span>

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

### <span data-ttu-id="b8dbd-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8dbd-134">-ResourceGroupName</span></span>
<span data-ttu-id="b8dbd-135">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b8dbd-135">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b8dbd-136">-Restart</span><span class="sxs-lookup"><span data-stu-id="b8dbd-136">-Restart</span></span>
<span data-ttu-id="b8dbd-137">Indica que esse cmdlet reinicia a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b8dbd-137">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="b8dbd-138">Uma reinicialização geralmente é necessária para fazer a mudança entrar em vigor.</span><span class="sxs-lookup"><span data-stu-id="b8dbd-138">A restart is often required to make the change effective.</span></span>

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

### <span data-ttu-id="b8dbd-139">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="b8dbd-139">-TypeHandlerVersion</span></span>
<span data-ttu-id="b8dbd-140">Especifica a versão da extensão do domínio.</span><span class="sxs-lookup"><span data-stu-id="b8dbd-140">Specifies the version of the domain extension.</span></span>

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

### <span data-ttu-id="b8dbd-141">-VMName</span><span class="sxs-lookup"><span data-stu-id="b8dbd-141">-VMName</span></span>
<span data-ttu-id="b8dbd-142">Especifica o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b8dbd-142">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="b8dbd-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b8dbd-143">-Confirm</span></span>
<span data-ttu-id="b8dbd-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8dbd-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8dbd-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8dbd-145">-WhatIf</span></span>
<span data-ttu-id="b8dbd-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b8dbd-146">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="b8dbd-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b8dbd-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8dbd-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8dbd-148">CommonParameters</span></span>
<span data-ttu-id="b8dbd-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8dbd-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8dbd-150">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8dbd-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8dbd-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b8dbd-151">INPUTS</span></span>

## <span data-ttu-id="b8dbd-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b8dbd-152">OUTPUTS</span></span>

## <span data-ttu-id="b8dbd-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b8dbd-153">NOTES</span></span>

## <span data-ttu-id="b8dbd-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8dbd-154">RELATED LINKS</span></span>

[<span data-ttu-id="b8dbd-155">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="b8dbd-155">Get-AzureRmVMADDomainExtension</span></span>](./Get-AzureRmVMADDomainExtension.md)
