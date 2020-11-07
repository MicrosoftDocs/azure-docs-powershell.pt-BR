---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2E363D6B-7A05-4C54-B005-68FDBA49A105
online version: ''
schema: 2.0.0
ms.openlocfilehash: cda64b916635d3b46ffb7e8b4170330810a95b5b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945942"
---
# <span data-ttu-id="83dc5-101">Stop-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="83dc5-101">Stop-AzureAutomationJob</span></span>

## <span data-ttu-id="83dc5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="83dc5-102">SYNOPSIS</span></span>

<span data-ttu-id="83dc5-103">Interrompe um trabalho de automação.</span><span class="sxs-lookup"><span data-stu-id="83dc5-103">Stops an Automation job.</span></span>

## <span data-ttu-id="83dc5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="83dc5-104">SYNTAX</span></span>

```
Stop-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="83dc5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="83dc5-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="83dc5-106">O cmdlet **Stop-AzureAutomationJob** interrompe um trabalho de automação do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="83dc5-106">The **Stop-AzureAutomationJob** cmdlet stops a Microsoft Azure Automation job.</span></span>
<span data-ttu-id="83dc5-107">Especifique um trabalho de automação em execução.</span><span class="sxs-lookup"><span data-stu-id="83dc5-107">Specify a running automation job.</span></span>

## <span data-ttu-id="83dc5-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="83dc5-108">EXAMPLES</span></span>

### <span data-ttu-id="83dc5-109">Exemplo 1: parar um trabalho</span><span class="sxs-lookup"><span data-stu-id="83dc5-109">Example 1: Stop a job</span></span>
```
PS C:\> Stop-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64
```

<span data-ttu-id="83dc5-110">Esse comando para o trabalho que tem a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="83dc5-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="83dc5-111">OS</span><span class="sxs-lookup"><span data-stu-id="83dc5-111">PARAMETERS</span></span>

### <span data-ttu-id="83dc5-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="83dc5-112">-AutomationAccountName</span></span>
<span data-ttu-id="83dc5-113">Especifica o nome de uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="83dc5-113">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="83dc5-114">-ID</span><span class="sxs-lookup"><span data-stu-id="83dc5-114">-Id</span></span>
<span data-ttu-id="83dc5-115">Especifica a ID de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="83dc5-115">Specifies the ID of a job.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83dc5-116">-Perfil</span><span class="sxs-lookup"><span data-stu-id="83dc5-116">-Profile</span></span>
<span data-ttu-id="83dc5-117">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="83dc5-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="83dc5-118">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="83dc5-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="83dc5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83dc5-119">CommonParameters</span></span>
<span data-ttu-id="83dc5-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83dc5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83dc5-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83dc5-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83dc5-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="83dc5-122">INPUTS</span></span>

## <span data-ttu-id="83dc5-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="83dc5-123">OUTPUTS</span></span>

## <span data-ttu-id="83dc5-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="83dc5-124">NOTES</span></span>

## <span data-ttu-id="83dc5-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="83dc5-125">RELATED LINKS</span></span>

[<span data-ttu-id="83dc5-126">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="83dc5-126">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="83dc5-127">Currículo-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="83dc5-127">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="83dc5-128">Suspender-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="83dc5-128">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)


