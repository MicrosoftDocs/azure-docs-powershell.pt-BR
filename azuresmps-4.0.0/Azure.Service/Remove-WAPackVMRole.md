---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9999E0EE-4A32-4C18-A6EC-2A073DC08710
online version: ''
schema: 2.0.0
ms.openlocfilehash: e5dfe0f42987ba51613ff9bafa000713456dfaf7
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93947411"
---
# <span data-ttu-id="5d374-101">Remove-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="5d374-101">Remove-WAPackVMRole</span></span>

## <span data-ttu-id="5d374-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5d374-102">SYNOPSIS</span></span>
<span data-ttu-id="5d374-103">Remove objetos de função de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5d374-103">Removes virtual machine role objects.</span></span>

## <span data-ttu-id="5d374-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5d374-104">SYNTAX</span></span>

### <span data-ttu-id="5d374-105">FromVMRoleObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="5d374-105">FromVMRoleObject (Default)</span></span>
```
Remove-WAPackVMRole -VMRole <VMRole> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5d374-106">FromCloudService</span><span class="sxs-lookup"><span data-stu-id="5d374-106">FromCloudService</span></span>
```
Remove-WAPackVMRole -VMRole <VMRole> -CloudServiceName <String> [-PassThru] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d374-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5d374-107">DESCRIPTION</span></span>
<span data-ttu-id="5d374-108">Esses tópicos são preteridos e serão removidos no futuro.</span><span class="sxs-lookup"><span data-stu-id="5d374-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="5d374-109">Este tópico descreve o cmdlet na versão 0.8.1 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5d374-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="5d374-110">Para descobrir a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="5d374-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="5d374-111">O cmdlet **Remove-WAPackVMRole** remove objetos de função da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5d374-111">The **Remove-WAPackVMRole** cmdlet removes virtual machine role objects.</span></span>

## <span data-ttu-id="5d374-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5d374-112">EXAMPLES</span></span>

### <span data-ttu-id="5d374-113">Exemplo 1: remover uma função de máquina virtual (que foi criada usando o portal de WAP)</span><span class="sxs-lookup"><span data-stu-id="5d374-113">Example 1: Remove a virtual machine role (which was created using the WAP portal)</span></span>
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole01"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole
```

<span data-ttu-id="5d374-114">O primeiro comando obtém a função da máquina virtual chamada ContosoVMRole01 usando o cmdlet **Get-WAPackVMRole** e armazena esse objeto na variável $VMRole.</span><span class="sxs-lookup"><span data-stu-id="5d374-114">The first command gets the virtual machine role named ContosoVMRole01 by using the **Get-WAPackVMRole** cmdlet, and then stores that object in the $VMRole variable.</span></span>

<span data-ttu-id="5d374-115">O segundo comando Remove a função de máquina virtual armazenada em $VMRole.</span><span class="sxs-lookup"><span data-stu-id="5d374-115">The second command removes the virtual machine role stored in $VMRole.</span></span>
<span data-ttu-id="5d374-116">O comando solicitará confirmação. Pressupondo que essa função da máquina virtual seja criada usando o portal de WAP, não é necessário especificar o nome do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="5d374-116">The command prompts you for confirmation.Assuming this virtual machine role was created using the WAP portal, there's no need to specify the cloud service name.</span></span>

### <span data-ttu-id="5d374-117">Exemplo 2: remover uma função de máquina virtual que foi criada após a criação manual de um serviço na nuvem</span><span class="sxs-lookup"><span data-stu-id="5d374-117">Example 2: Remove a virtual machine role which was created after manually creating a cloud service</span></span>
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole02"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -CloudServiceName "ContosoCloudService02"
```

<span data-ttu-id="5d374-118">O primeiro comando obtém a função da máquina virtual chamada "ContosoVMRole02" usando o cmdlet **Get-WAPackVMRole** e armazena esse objeto na variável $VMRole.</span><span class="sxs-lookup"><span data-stu-id="5d374-118">The first command gets the virtual machine role named "ContosoVMRole02" by using the **Get-WAPackVMRole** cmdlet, and then stores that object in the $VMRole variable.</span></span>

<span data-ttu-id="5d374-119">O segundo comando Remove a função de máquina virtual armazenada em $VMRole.</span><span class="sxs-lookup"><span data-stu-id="5d374-119">The second command removes the virtual machine role stored in $VMRole.</span></span>
<span data-ttu-id="5d374-120">O comando solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="5d374-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="5d374-121">Pressupondo que essa função da máquina virtual não foi criada usando o portal, o usuário precisa especificar o nome do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="5d374-121">Assuming this virtual machine role was not created using the portal, the user needs to specify the cloud service name.</span></span>
<span data-ttu-id="5d374-122">Nesse caso, chamado "ContosoCloudService02".</span><span class="sxs-lookup"><span data-stu-id="5d374-122">In this case named "ContosoCloudService02".</span></span>

### <span data-ttu-id="5d374-123">Exemplo 3: remover uma função de máquina virtual sem confirmação</span><span class="sxs-lookup"><span data-stu-id="5d374-123">Example 3: Remove a virtual machine role without confirmation</span></span>
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole03"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -Force
```

<span data-ttu-id="5d374-124">O primeiro comando obtém o serviço de nuvem chamado ContosoVMRole03 usando o cmdlet **Get-WAPackVMRole** e armazena esse objeto na variável $VMRole.</span><span class="sxs-lookup"><span data-stu-id="5d374-124">The first command gets the cloud service named ContosoVMRole03 by using the **Get-WAPackVMRole** cmdlet, and then stores that object in the $VMRole variable.</span></span>

<span data-ttu-id="5d374-125">O segundo comando Remove a função de máquina virtual armazenada em $VMRole.</span><span class="sxs-lookup"><span data-stu-id="5d374-125">The second command removes the virtual machine role stored in $VMRole.</span></span>
<span data-ttu-id="5d374-126">Esse comando inclui o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="5d374-126">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="5d374-127">O comando não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="5d374-127">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="5d374-128">OS</span><span class="sxs-lookup"><span data-stu-id="5d374-128">PARAMETERS</span></span>

### <span data-ttu-id="5d374-129">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="5d374-129">-CloudServiceName</span></span>
<span data-ttu-id="5d374-130">Especifica o nome do serviço em nuvem da função da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5d374-130">Specifies the cloud service name of virtual machine role.</span></span>

```yaml
Type: String
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d374-131">-Force</span><span class="sxs-lookup"><span data-stu-id="5d374-131">-Force</span></span>
<span data-ttu-id="5d374-132">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="5d374-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5d374-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d374-133">-PassThru</span></span>
<span data-ttu-id="5d374-134">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="5d374-134">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5d374-135">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="5d374-135">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5d374-136">-Perfil</span><span class="sxs-lookup"><span data-stu-id="5d374-136">-Profile</span></span>
<span data-ttu-id="5d374-137">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="5d374-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5d374-138">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="5d374-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d374-139">-VMRole</span><span class="sxs-lookup"><span data-stu-id="5d374-139">-VMRole</span></span>
<span data-ttu-id="5d374-140">Especifica uma função de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5d374-140">Specifies a virtual machine role.</span></span>
<span data-ttu-id="5d374-141">Para obter uma função de máquina virtual, use o cmdlet **Get-WAPackVMRole** .</span><span class="sxs-lookup"><span data-stu-id="5d374-141">To get a virtual machine role, use the **Get-WAPackVMRole** cmdlet.</span></span>

```yaml
Type: VMRole
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d374-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5d374-142">-Confirm</span></span>
<span data-ttu-id="5d374-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d374-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d374-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d374-144">-WhatIf</span></span>
<span data-ttu-id="5d374-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5d374-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d374-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5d374-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d374-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d374-147">CommonParameters</span></span>
<span data-ttu-id="5d374-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d374-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d374-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d374-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d374-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5d374-150">INPUTS</span></span>

## <span data-ttu-id="5d374-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5d374-151">OUTPUTS</span></span>

## <span data-ttu-id="5d374-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5d374-152">NOTES</span></span>

## <span data-ttu-id="5d374-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5d374-153">RELATED LINKS</span></span>

[<span data-ttu-id="5d374-154">Get-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="5d374-154">Get-WAPackVMRole</span></span>](./Get-WAPackVMRole.md)

[<span data-ttu-id="5d374-155">New-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="5d374-155">New-WAPackVMRole</span></span>](./New-WAPackVMRole.md)

[<span data-ttu-id="5d374-156">Set-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="5d374-156">Set-WAPackVMRole</span></span>](./Set-WAPackVMRole.md)


