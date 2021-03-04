---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/powershell/module/az.communication/new-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationService.md
ms.openlocfilehash: 8382358e6bad15948ed8cdfeb904cf8c431bd131
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890470"
---
# <span data-ttu-id="9f1d2-101">New-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="9f1d2-101">New-AzCommunicationService</span></span>

## <span data-ttu-id="9f1d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f1d2-102">SYNOPSIS</span></span>
<span data-ttu-id="9f1d2-103">Crie um novo CommunicationService ou atualize um CommunicationService existente.</span><span class="sxs-lookup"><span data-stu-id="9f1d2-103">Create a new CommunicationService or update an existing CommunicationService.</span></span>

## <span data-ttu-id="9f1d2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9f1d2-104">SYNTAX</span></span>

```
New-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DataLocation <String>] [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9f1d2-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9f1d2-105">DESCRIPTION</span></span>
<span data-ttu-id="9f1d2-106">Crie um novo CommunicationService ou atualize um CommunicationService existente.</span><span class="sxs-lookup"><span data-stu-id="9f1d2-106">Create a new CommunicationService or update an existing CommunicationService.</span></span>

## <span data-ttu-id="9f1d2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9f1d2-107">EXAMPLES</span></span>

### <span data-ttu-id="9f1d2-108">Exemplo 1: Criar um recurso do ACS</span><span class="sxs-lookup"><span data-stu-id="9f1d2-108">Example 1: Create a ACS resource</span></span>
```powershell
PS C:\> New-AzCommunicationService -ResourceGroupName ContosoResourceProvider1 -Name ContosoAcsResource1 -DataLocation UnitedStates -Location Global

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="9f1d2-109">Cria um recurso ACS usando os parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="9f1d2-109">Creates a ACS resource using the specified parameters.</span></span>

## <span data-ttu-id="9f1d2-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9f1d2-110">PARAMETERS</span></span>

### <span data-ttu-id="9f1d2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f1d2-111">-AsJob</span></span>
<span data-ttu-id="9f1d2-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="9f1d2-112">Run the command as a job</span></span>

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

### <span data-ttu-id="9f1d2-113">-DataLocation</span><span class="sxs-lookup"><span data-stu-id="9f1d2-113">-DataLocation</span></span>
<span data-ttu-id="9f1d2-114">O local onde o serviço de comunicação armazena seus dados em repouso.</span><span class="sxs-lookup"><span data-stu-id="9f1d2-114">The location where the communication service stores its data at rest.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f1d2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f1d2-115">-DefaultProfile</span></span>
<span data-ttu-id="9f1d2-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9f1d2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f1d2-117">-Location</span><span class="sxs-lookup"><span data-stu-id="9f1d2-117">-Location</span></span>
<span data-ttu-id="9f1d2-118">O local do Azure onde o CommunicationService está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="9f1d2-118">The Azure location where the CommunicationService is running.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f1d2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="9f1d2-119">-Name</span></span>
<span data-ttu-id="9f1d2-120">O nome do recurso CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="9f1d2-120">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f1d2-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9f1d2-121">-NoWait</span></span>
<span data-ttu-id="9f1d2-122">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="9f1d2-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9f1d2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f1d2-123">-ResourceGroupName</span></span>
<span data-ttu-id="9f1d2-124">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="9f1d2-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="9f1d2-125">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="9f1d2-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f1d2-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9f1d2-126">-SubscriptionId</span></span>
<span data-ttu-id="9f1d2-127">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9f1d2-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="9f1d2-128">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="9f1d2-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f1d2-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="9f1d2-129">-Tag</span></span>
<span data-ttu-id="9f1d2-130">Marcas do serviço que é uma lista de pares de valores-chave que descrevem o recurso.</span><span class="sxs-lookup"><span data-stu-id="9f1d2-130">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f1d2-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f1d2-131">-Confirm</span></span>
<span data-ttu-id="9f1d2-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f1d2-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f1d2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f1d2-133">-WhatIf</span></span>
<span data-ttu-id="9f1d2-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9f1d2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f1d2-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9f1d2-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f1d2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f1d2-136">CommonParameters</span></span>
<span data-ttu-id="9f1d2-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f1d2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f1d2-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f1d2-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f1d2-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9f1d2-139">INPUTS</span></span>

## <span data-ttu-id="9f1d2-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9f1d2-140">OUTPUTS</span></span>

### <span data-ttu-id="9f1d2-141">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="9f1d2-141">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="9f1d2-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="9f1d2-142">NOTES</span></span>

<span data-ttu-id="9f1d2-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="9f1d2-143">ALIASES</span></span>

## <span data-ttu-id="9f1d2-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f1d2-144">RELATED LINKS</span></span>

