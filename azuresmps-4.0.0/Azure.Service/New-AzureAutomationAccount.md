---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 59CDE74B-EFB3-4904-A482-466B0EA17F4B
online version: ''
schema: 2.0.0
ms.openlocfilehash: a787193669cab32a43b7c9b9eb2010a6e545539b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946224"
---
# <span data-ttu-id="fa827-101">New-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="fa827-101">New-AzureAutomationAccount</span></span>

## <span data-ttu-id="fa827-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fa827-102">SYNOPSIS</span></span>

<span data-ttu-id="fa827-103">Cria uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="fa827-103">Creates an Automation account.</span></span>

## <span data-ttu-id="fa827-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fa827-104">SYNTAX</span></span>

```
New-AzureAutomationAccount -Name <String> -Location <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fa827-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fa827-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="fa827-106">O cmdlet **New-AzureAutomationAccount** cria uma nova conta na automação do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fa827-106">The **New-AzureAutomationAccount** cmdlet creates a new account in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="fa827-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fa827-107">EXAMPLES</span></span>

### <span data-ttu-id="fa827-108">Exemplo 1: criar uma conta de automação</span><span class="sxs-lookup"><span data-stu-id="fa827-108">Example 1: Create an Automation account</span></span>
```
PS C:\> New-AzureAutomationAccount -Name "MyAutomationAccount" -Location "East US"
```

<span data-ttu-id="fa827-109">Esse comando cria uma conta de automação chamada MyAutomationAccount na região leste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="fa827-109">This command creates an Automation account named MyAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="fa827-110">OS</span><span class="sxs-lookup"><span data-stu-id="fa827-110">PARAMETERS</span></span>

### <span data-ttu-id="fa827-111">-Local</span><span class="sxs-lookup"><span data-stu-id="fa827-111">-Location</span></span>
<span data-ttu-id="fa827-112">Especifica o local da conta.</span><span class="sxs-lookup"><span data-stu-id="fa827-112">Specifies the location of the account.</span></span>

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

### <span data-ttu-id="fa827-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="fa827-113">-Name</span></span>
<span data-ttu-id="fa827-114">Especifica o nome da conta.</span><span class="sxs-lookup"><span data-stu-id="fa827-114">Specifies the name of the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa827-115">-Perfil</span><span class="sxs-lookup"><span data-stu-id="fa827-115">-Profile</span></span>
<span data-ttu-id="fa827-116">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="fa827-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fa827-117">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="fa827-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fa827-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa827-118">CommonParameters</span></span>
<span data-ttu-id="fa827-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa827-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa827-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa827-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa827-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fa827-121">INPUTS</span></span>

## <span data-ttu-id="fa827-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fa827-122">OUTPUTS</span></span>

### <span data-ttu-id="fa827-123">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="fa827-123">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="fa827-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fa827-124">NOTES</span></span>

## <span data-ttu-id="fa827-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fa827-125">RELATED LINKS</span></span>

[<span data-ttu-id="fa827-126">Get-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="fa827-126">Get-AzureAutomationAccount</span></span>](./Get-AzureAutomationAccount.md)

[<span data-ttu-id="fa827-127">Remove-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="fa827-127">Remove-AzureAutomationAccount</span></span>](./Remove-AzureAutomationAccount.md)


