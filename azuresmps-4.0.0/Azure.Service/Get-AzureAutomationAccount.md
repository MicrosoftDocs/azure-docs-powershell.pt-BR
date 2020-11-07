---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 7B2D9768-919B-4F54-BBC7-8882CC2C973A
online version: ''
schema: 2.0.0
ms.openlocfilehash: a9ce55e573881a29291085e9bf25381170bbf052
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946371"
---
# <span data-ttu-id="838d9-101">Get-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="838d9-101">Get-AzureAutomationAccount</span></span>

## <span data-ttu-id="838d9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="838d9-102">SYNOPSIS</span></span>

<span data-ttu-id="838d9-103">Obtém contas de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="838d9-103">Gets Azure Automation accounts.</span></span>

## <span data-ttu-id="838d9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="838d9-104">SYNTAX</span></span>

```
Get-AzureAutomationAccount [-Name <String>] [-Location <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="838d9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="838d9-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="838d9-106">O cmdlet **Get-AzureAutomationAccount** Obtém as contas de automação do Microsoft Azure para a sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="838d9-106">The **Get-AzureAutomationAccount** cmdlet gets the Microsoft Azure Automation accounts for your subscription.</span></span>
<span data-ttu-id="838d9-107">Uma conta de automação é um contêiner de recursos de automação que é isolado dos recursos de outras contas de automação.</span><span class="sxs-lookup"><span data-stu-id="838d9-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span>
<span data-ttu-id="838d9-108">Os recursos de automação incluem runbooks, trabalhos e ativos.</span><span class="sxs-lookup"><span data-stu-id="838d9-108">Automation resources include runbooks, jobs, and assets.</span></span>

## <span data-ttu-id="838d9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="838d9-109">EXAMPLES</span></span>

### <span data-ttu-id="838d9-110">Exemplo 1: obter uma conta de automação</span><span class="sxs-lookup"><span data-stu-id="838d9-110">Example 1: Get an Automation account</span></span>
```
PS C:\> Get-AzureAutomationAccount -Name "Contoso17"
```

<span data-ttu-id="838d9-111">Esse comando obtém a conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="838d9-111">This command gets the Automation account named Contoso17.</span></span>

## <span data-ttu-id="838d9-112">OS</span><span class="sxs-lookup"><span data-stu-id="838d9-112">PARAMETERS</span></span>

### <span data-ttu-id="838d9-113">-Local</span><span class="sxs-lookup"><span data-stu-id="838d9-113">-Location</span></span>
<span data-ttu-id="838d9-114">Especifica um local do Azure associado a contas de automação.</span><span class="sxs-lookup"><span data-stu-id="838d9-114">Specifies an Azure location associated with Automation accounts.</span></span>

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

### <span data-ttu-id="838d9-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="838d9-115">-Name</span></span>
<span data-ttu-id="838d9-116">Especifica o nome de uma conta de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="838d9-116">Specifies the name of an Azure Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="838d9-117">-Perfil</span><span class="sxs-lookup"><span data-stu-id="838d9-117">-Profile</span></span>
<span data-ttu-id="838d9-118">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="838d9-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="838d9-119">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="838d9-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="838d9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="838d9-120">CommonParameters</span></span>
<span data-ttu-id="838d9-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="838d9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="838d9-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="838d9-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="838d9-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="838d9-123">INPUTS</span></span>

## <span data-ttu-id="838d9-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="838d9-124">OUTPUTS</span></span>

### <span data-ttu-id="838d9-125">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="838d9-125">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="838d9-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="838d9-126">NOTES</span></span>

## <span data-ttu-id="838d9-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="838d9-127">RELATED LINKS</span></span>

[<span data-ttu-id="838d9-128">New-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="838d9-128">New-AzureAutomationAccount</span></span>](./New-AzureAutomationAccount.md)

[<span data-ttu-id="838d9-129">Remove-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="838d9-129">Remove-AzureAutomationAccount</span></span>](./Remove-AzureAutomationAccount.md)


