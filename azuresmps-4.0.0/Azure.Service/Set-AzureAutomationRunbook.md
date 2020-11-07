---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C24CFC83-3151-452D-A7B9-E78466493474
online version: ''
schema: 2.0.0
ms.openlocfilehash: e193dba6f64553e5e52d7f900bdc5c54deac5112
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946072"
---
# <span data-ttu-id="e60e9-101">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e60e9-101">Set-AzureAutomationRunbook</span></span>

## <span data-ttu-id="e60e9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e60e9-102">SYNOPSIS</span></span>

<span data-ttu-id="e60e9-103">Modifica a configuração de um runbook.</span><span class="sxs-lookup"><span data-stu-id="e60e9-103">Modifies the configuration of a runbook.</span></span>

## <span data-ttu-id="e60e9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e60e9-104">SYNTAX</span></span>

```
Set-AzureAutomationRunbook -Name <String> [-Description <String>] [-Tags <String[]>] [-LogProgress <Boolean>]
 [-LogVerbose <Boolean>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e60e9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e60e9-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="e60e9-106">O cmdlet **set-AzureAutomationRunbook** modifica a configuração de um runbook de automação do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e60e9-106">The **Set-AzureAutomationRunbook** cmdlet modifies the configuration of a Microsoft Azure Automation runbook.</span></span>

## <span data-ttu-id="e60e9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e60e9-107">EXAMPLES</span></span>

### <span data-ttu-id="e60e9-108">Exemplo 1: habilitar o registro em log detalhado para um runbook</span><span class="sxs-lookup"><span data-stu-id="e60e9-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\> Set-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "MyRunbook" -LogVerbose $True
```

<span data-ttu-id="e60e9-109">Esse comando habilita o registro em log detalhado para os trabalhos do runbook especificado na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="e60e9-109">This command enables verbose logging for the jobs of the specified runbook in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="e60e9-110">OS</span><span class="sxs-lookup"><span data-stu-id="e60e9-110">PARAMETERS</span></span>

### <span data-ttu-id="e60e9-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e60e9-111">-AutomationAccountName</span></span>
<span data-ttu-id="e60e9-112">Especifica o nome de uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="e60e9-112">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="e60e9-113">-Descrição</span><span class="sxs-lookup"><span data-stu-id="e60e9-113">-Description</span></span>
<span data-ttu-id="e60e9-114">Especifica uma descrição para o runbook.</span><span class="sxs-lookup"><span data-stu-id="e60e9-114">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="e60e9-115">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="e60e9-115">-LogProgress</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e60e9-116">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="e60e9-116">-LogVerbose</span></span>
<span data-ttu-id="e60e9-117">Indica se o registro detalhado deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="e60e9-117">Indicates whether to use verbose logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e60e9-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="e60e9-118">-Name</span></span>
<span data-ttu-id="e60e9-119">Especifica um nome.</span><span class="sxs-lookup"><span data-stu-id="e60e9-119">Specifies a name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e60e9-120">-Perfil</span><span class="sxs-lookup"><span data-stu-id="e60e9-120">-Profile</span></span>
<span data-ttu-id="e60e9-121">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="e60e9-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e60e9-122">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="e60e9-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e60e9-123">-Marcas</span><span class="sxs-lookup"><span data-stu-id="e60e9-123">-Tags</span></span>
<span data-ttu-id="e60e9-124">Especifica uma matriz de marcas.</span><span class="sxs-lookup"><span data-stu-id="e60e9-124">Specifies an array of tags.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e60e9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e60e9-125">CommonParameters</span></span>
<span data-ttu-id="e60e9-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e60e9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e60e9-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e60e9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e60e9-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e60e9-128">INPUTS</span></span>

## <span data-ttu-id="e60e9-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e60e9-129">OUTPUTS</span></span>

### <span data-ttu-id="e60e9-130">Microsoft. Azure. Commands. Automation. Model. runbook</span><span class="sxs-lookup"><span data-stu-id="e60e9-130">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="e60e9-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e60e9-131">NOTES</span></span>

## <span data-ttu-id="e60e9-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e60e9-132">RELATED LINKS</span></span>

[<span data-ttu-id="e60e9-133">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e60e9-133">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="e60e9-134">New-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e60e9-134">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="e60e9-135">Publicar-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e60e9-135">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="e60e9-136">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e60e9-136">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="e60e9-137">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e60e9-137">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


