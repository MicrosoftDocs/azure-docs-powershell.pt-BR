---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/new-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationService.md
ms.openlocfilehash: 821590b158478c38e5d4e997254e98a802d4befd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434402"
---
# <span data-ttu-id="152ba-101">New-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="152ba-101">New-AzCommunicationService</span></span>

## <span data-ttu-id="152ba-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="152ba-102">SYNOPSIS</span></span>
<span data-ttu-id="152ba-103">Crie um novo CommunicationService ou atualize um CommunicationService existente.</span><span class="sxs-lookup"><span data-stu-id="152ba-103">Create a new CommunicationService or update an existing CommunicationService.</span></span>

## <span data-ttu-id="152ba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="152ba-104">SYNTAX</span></span>

```
New-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DataLocation <String>] [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="152ba-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="152ba-105">DESCRIPTION</span></span>
<span data-ttu-id="152ba-106">Crie um novo CommunicationService ou atualize um CommunicationService existente.</span><span class="sxs-lookup"><span data-stu-id="152ba-106">Create a new CommunicationService or update an existing CommunicationService.</span></span>

## <span data-ttu-id="152ba-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="152ba-107">EXAMPLES</span></span>

### <span data-ttu-id="152ba-108">Exemplo 1: criar um recurso ACS</span><span class="sxs-lookup"><span data-stu-id="152ba-108">Example 1: Create a ACS resource</span></span>
```powershell
PS C:\> New-AzCommunicationService -ResourceGroupName ContosoResourceProvider1 -Name ContosoAcsResource1 -DataLocation UnitedStates -Location Global

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="152ba-109">Cria um recurso ACS usando os parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="152ba-109">Creates a ACS resource using the specified parameters.</span></span>

## <span data-ttu-id="152ba-110">OS</span><span class="sxs-lookup"><span data-stu-id="152ba-110">PARAMETERS</span></span>

### <span data-ttu-id="152ba-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="152ba-111">-AsJob</span></span>
<span data-ttu-id="152ba-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="152ba-112">Run the command as a job</span></span>

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

### <span data-ttu-id="152ba-113">-Local do DataSerial</span><span class="sxs-lookup"><span data-stu-id="152ba-113">-DataLocation</span></span>
<span data-ttu-id="152ba-114">O local em que o serviço de comunicação armazena seus dados em repouso.</span><span class="sxs-lookup"><span data-stu-id="152ba-114">The location where the communication service stores its data at rest.</span></span>

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

### <span data-ttu-id="152ba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="152ba-115">-DefaultProfile</span></span>
<span data-ttu-id="152ba-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="152ba-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="152ba-117">-Local</span><span class="sxs-lookup"><span data-stu-id="152ba-117">-Location</span></span>
<span data-ttu-id="152ba-118">O local do Azure onde o CommunicationService está em execução.</span><span class="sxs-lookup"><span data-stu-id="152ba-118">The Azure location where the CommunicationService is running.</span></span>

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

### <span data-ttu-id="152ba-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="152ba-119">-Name</span></span>
<span data-ttu-id="152ba-120">O nome do recurso CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="152ba-120">The name of the CommunicationService resource.</span></span>

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

### <span data-ttu-id="152ba-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="152ba-121">-NoWait</span></span>
<span data-ttu-id="152ba-122">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="152ba-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="152ba-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="152ba-123">-ResourceGroupName</span></span>
<span data-ttu-id="152ba-124">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="152ba-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="152ba-125">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="152ba-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="152ba-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="152ba-126">-SubscriptionId</span></span>
<span data-ttu-id="152ba-127">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="152ba-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="152ba-128">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="152ba-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="152ba-129">-Marca</span><span class="sxs-lookup"><span data-stu-id="152ba-129">-Tag</span></span>
<span data-ttu-id="152ba-130">Marcas do serviço que é uma lista de pares de valores chave que descrevem o recurso.</span><span class="sxs-lookup"><span data-stu-id="152ba-130">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="152ba-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="152ba-131">-Confirm</span></span>
<span data-ttu-id="152ba-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="152ba-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="152ba-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="152ba-133">-WhatIf</span></span>
<span data-ttu-id="152ba-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="152ba-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="152ba-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="152ba-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="152ba-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="152ba-136">CommonParameters</span></span>
<span data-ttu-id="152ba-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="152ba-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="152ba-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="152ba-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="152ba-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="152ba-139">INPUTS</span></span>

## <span data-ttu-id="152ba-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="152ba-140">OUTPUTS</span></span>

### <span data-ttu-id="152ba-141">Microsoft. Azure. PowerShell. cmdlets. Communication. Models. Api20200820Preview. ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="152ba-141">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="152ba-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="152ba-142">NOTES</span></span>

<span data-ttu-id="152ba-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="152ba-143">ALIASES</span></span>

## <span data-ttu-id="152ba-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="152ba-144">RELATED LINKS</span></span>

