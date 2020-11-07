---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1ECF6BB5-3751-4DA0-AC6C-A64F15F46D26
online version: ''
schema: 2.0.0
ms.openlocfilehash: 552c2511a806abb4329860e7c15d8a68b5e03f79
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93947413"
---
# <span data-ttu-id="b3fb1-101">Remove-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="b3fb1-101">Remove-WAPackCloudService</span></span>

## <span data-ttu-id="b3fb1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b3fb1-102">SYNOPSIS</span></span>
<span data-ttu-id="b3fb1-103">Remove objetos de serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="b3fb1-103">Removes cloud service objects.</span></span>

## <span data-ttu-id="b3fb1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b3fb1-104">SYNTAX</span></span>

```
Remove-WAPackCloudService -CloudService <CloudService> [-PassThru] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3fb1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b3fb1-105">DESCRIPTION</span></span>
<span data-ttu-id="b3fb1-106">Esses tópicos são preteridos e serão removidos no futuro.</span><span class="sxs-lookup"><span data-stu-id="b3fb1-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="b3fb1-107">Este tópico descreve o cmdlet na versão 0.8.1 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b3fb1-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b3fb1-108">Para descobrir a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="b3fb1-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="b3fb1-109">O cmdlet **Remove-WAPackCloudService** remove objetos de serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="b3fb1-109">The **Remove-WAPackCloudService** cmdlet removes cloud service objects.</span></span>

## <span data-ttu-id="b3fb1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b3fb1-110">EXAMPLES</span></span>

### <span data-ttu-id="b3fb1-111">Exemplo 1: remover um serviço na nuvem</span><span class="sxs-lookup"><span data-stu-id="b3fb1-111">Example 1: Remove a cloud service</span></span>
```
PS C:\> $CloudService = Get-WAPackCloudService -Name "ContosoCloudService01"
PS C:\> Remove-WAPackVM -VM $CloudService
```

<span data-ttu-id="b3fb1-112">O primeiro comando obtém o serviço de nuvem chamado ContosoCloudService01 usando o cmdlet **Get-WAPackCloudService** e armazena esse objeto na variável $CloudService.</span><span class="sxs-lookup"><span data-stu-id="b3fb1-112">The first command gets the cloud service named ContosoCloudService01 by using the **Get-WAPackCloudService** cmdlet, and then stores that object in the $CloudService variable.</span></span>

<span data-ttu-id="b3fb1-113">O segundo comando Remove a cloudservice armazenada em $CloudService.</span><span class="sxs-lookup"><span data-stu-id="b3fb1-113">The second command removes the cloudservice stored in $CloudService.</span></span>
<span data-ttu-id="b3fb1-114">O comando solicitará confirmação.</span><span class="sxs-lookup"><span data-stu-id="b3fb1-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="b3fb1-115">Exemplo 2: remover um serviço de nuvem sem confirmação</span><span class="sxs-lookup"><span data-stu-id="b3fb1-115">Example 2: Remove a cloud service without confirmation</span></span>
```
PS C:\> $CloudService = Get-WAPackCloudService -Name "ContosoCloudService02"
PS C:\> Remove-WAPackCloudService -VM $CloudService -Force
```

<span data-ttu-id="b3fb1-116">O primeiro comando obtém o serviço de nuvem chamado ContosoCloudService02 usando o cmdlet **Get-WAPackCloudService** e armazena esse objeto na variável $CloudService.</span><span class="sxs-lookup"><span data-stu-id="b3fb1-116">The first command gets the cloud service named ContosoCloudService02 by using the **Get-WAPackCloudService** cmdlet, and then stores that object in the $CloudService variable.</span></span>

<span data-ttu-id="b3fb1-117">O segundo comando Remove o serviço na nuvem armazenado em $CloudService.</span><span class="sxs-lookup"><span data-stu-id="b3fb1-117">The second command removes the cloud service stored in $CloudService.</span></span>
<span data-ttu-id="b3fb1-118">Esse comando inclui o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="b3fb1-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="b3fb1-119">O comando não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="b3fb1-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="b3fb1-120">OS</span><span class="sxs-lookup"><span data-stu-id="b3fb1-120">PARAMETERS</span></span>

### <span data-ttu-id="b3fb1-121">-CloudService</span><span class="sxs-lookup"><span data-stu-id="b3fb1-121">-CloudService</span></span>
<span data-ttu-id="b3fb1-122">Especifica um objeto de serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="b3fb1-122">Specifies a cloud service object.</span></span>
<span data-ttu-id="b3fb1-123">Para obter um serviço na nuvem, use o cmdlet **Get-WAPackCloudService** .</span><span class="sxs-lookup"><span data-stu-id="b3fb1-123">To obtain a cloud service, use the **Get-WAPackCloudService** cmdlet.</span></span>

```yaml
Type: CloudService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3fb1-124">-Force</span><span class="sxs-lookup"><span data-stu-id="b3fb1-124">-Force</span></span>
<span data-ttu-id="b3fb1-125">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="b3fb1-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b3fb1-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3fb1-126">-PassThru</span></span>
<span data-ttu-id="b3fb1-127">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="b3fb1-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b3fb1-128">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="b3fb1-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b3fb1-129">-Perfil</span><span class="sxs-lookup"><span data-stu-id="b3fb1-129">-Profile</span></span>
<span data-ttu-id="b3fb1-130">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="b3fb1-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b3fb1-131">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="b3fb1-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b3fb1-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b3fb1-132">-Confirm</span></span>
<span data-ttu-id="b3fb1-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3fb1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3fb1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3fb1-134">-WhatIf</span></span>
<span data-ttu-id="b3fb1-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b3fb1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3fb1-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b3fb1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3fb1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3fb1-137">CommonParameters</span></span>
<span data-ttu-id="b3fb1-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3fb1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3fb1-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3fb1-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3fb1-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b3fb1-140">INPUTS</span></span>

## <span data-ttu-id="b3fb1-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b3fb1-141">OUTPUTS</span></span>

## <span data-ttu-id="b3fb1-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b3fb1-142">NOTES</span></span>

## <span data-ttu-id="b3fb1-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b3fb1-143">RELATED LINKS</span></span>

[<span data-ttu-id="b3fb1-144">Get-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="b3fb1-144">Get-WAPackCloudService</span></span>](./Get-WAPackCloudService.md)

[<span data-ttu-id="b3fb1-145">New-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="b3fb1-145">New-WAPackCloudService</span></span>](./New-WAPackCloudService.md)


