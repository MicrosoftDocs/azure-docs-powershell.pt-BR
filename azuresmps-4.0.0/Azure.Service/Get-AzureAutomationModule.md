---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 73F90276-FABD-414A-B29D-83F371C1ED21
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0544b4d5fafcb388b65271e736f43a15f02980c5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946368"
---
# <span data-ttu-id="99a9c-101">Get-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="99a9c-101">Get-AzureAutomationModule</span></span>

## <span data-ttu-id="99a9c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="99a9c-102">SYNOPSIS</span></span>

<span data-ttu-id="99a9c-103">Obter um módulo de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="99a9c-103">Get an Azure Automation module.</span></span>

## <span data-ttu-id="99a9c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99a9c-104">SYNTAX</span></span>

### <span data-ttu-id="99a9c-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="99a9c-105">ByAll (Default)</span></span>
```
Get-AzureAutomationModule -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="99a9c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="99a9c-106">ByName</span></span>
```
Get-AzureAutomationModule -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="99a9c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="99a9c-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="99a9c-108">O cmdlet **Get-AzureAutomationModule** Obtém um ou mais módulos de automação do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="99a9c-108">The **Get-AzureAutomationModule** cmdlet gets one or more Microsoft Azure Automation modules.</span></span>
<span data-ttu-id="99a9c-109">Por padrão, todos os módulos são retornados.</span><span class="sxs-lookup"><span data-stu-id="99a9c-109">By default, all modules are returned.</span></span>
<span data-ttu-id="99a9c-110">Para obter um módulo específico, especifique seu nome.</span><span class="sxs-lookup"><span data-stu-id="99a9c-110">To get a specific module, specify its name.</span></span>

## <span data-ttu-id="99a9c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="99a9c-111">EXAMPLES</span></span>

### <span data-ttu-id="99a9c-112">Exemplo 1: obter todos os módulos</span><span class="sxs-lookup"><span data-stu-id="99a9c-112">Example 1: Get all modules</span></span>
```
PS C:\> Get-AzureAutomationModule -AutomationAccountName "Contoso17"
```

<span data-ttu-id="99a9c-113">Esse comando obtém todos os módulos na conta de automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="99a9c-113">This command gets all modules in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="99a9c-114">Exemplo 2: obter um módulo</span><span class="sxs-lookup"><span data-stu-id="99a9c-114">Example 2: Get a module</span></span>
```
PS C:\> Get-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule"
```

<span data-ttu-id="99a9c-115">Esse comando obtém um módulo chamado ContosoModule na conta de automação do Azure chamado Contoso17.</span><span class="sxs-lookup"><span data-stu-id="99a9c-115">This command gets a module named ContosoModule in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="99a9c-116">OS</span><span class="sxs-lookup"><span data-stu-id="99a9c-116">PARAMETERS</span></span>

### <span data-ttu-id="99a9c-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="99a9c-117">-AutomationAccountName</span></span>
<span data-ttu-id="99a9c-118">Especifica o nome da conta de automação com o runbook a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="99a9c-118">Specifies the name of the Automation account with the runbook to retrieve.</span></span>

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

### <span data-ttu-id="99a9c-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="99a9c-119">-Name</span></span>
<span data-ttu-id="99a9c-120">Especifica o nome de um módulo a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="99a9c-120">Specifies the name of a module to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99a9c-121">-Perfil</span><span class="sxs-lookup"><span data-stu-id="99a9c-121">-Profile</span></span>
<span data-ttu-id="99a9c-122">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="99a9c-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="99a9c-123">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="99a9c-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="99a9c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99a9c-124">CommonParameters</span></span>
<span data-ttu-id="99a9c-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99a9c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99a9c-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99a9c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99a9c-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="99a9c-127">INPUTS</span></span>

## <span data-ttu-id="99a9c-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="99a9c-128">OUTPUTS</span></span>

### <span data-ttu-id="99a9c-129">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="99a9c-129">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="99a9c-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="99a9c-130">NOTES</span></span>

## <span data-ttu-id="99a9c-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="99a9c-131">RELATED LINKS</span></span>

[<span data-ttu-id="99a9c-132">New-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="99a9c-132">New-AzureAutomationModule</span></span>](./New-AzureAutomationModule.md)

[<span data-ttu-id="99a9c-133">Remove-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="99a9c-133">Remove-AzureAutomationModule</span></span>](./Remove-AzureAutomationModule.md)

[<span data-ttu-id="99a9c-134">Set-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="99a9c-134">Set-AzureAutomationModule</span></span>](./Set-AzureAutomationModule.md)


