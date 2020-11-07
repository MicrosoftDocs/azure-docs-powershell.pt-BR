---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: F80F20B6-21CB-4A37-9CBC-277F6EE99D4B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 421e33bbc74cd70ae6959feb93a0f95f6eac1caf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946427"
---
# <span data-ttu-id="4cced-101">Set-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="4cced-101">Set-AzureAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="4cced-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4cced-102">SYNOPSIS</span></span>

<span data-ttu-id="4cced-103">Modifica o valor de um campo para uma conexão.</span><span class="sxs-lookup"><span data-stu-id="4cced-103">Modifies the value of a field for a connection.</span></span>

## <span data-ttu-id="4cced-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4cced-104">SYNTAX</span></span>

```
Set-AzureAutomationConnectionFieldValue -Name <String> -ConnectionFieldName <String> -Value <Object>
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4cced-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4cced-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="4cced-106">O cmdlet **set-AzureAutomationConnectionFieldValue** modifica o valor de um campo para uma conexão na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="4cced-106">The **Set-AzureAutomationConnectionFieldValue** cmdlet modifies the value for a field for a connection in Azure Automation.</span></span>

## <span data-ttu-id="4cced-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4cced-107">EXAMPLES</span></span>

## <span data-ttu-id="4cced-108">OS</span><span class="sxs-lookup"><span data-stu-id="4cced-108">PARAMETERS</span></span>

### <span data-ttu-id="4cced-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4cced-109">-AutomationAccountName</span></span>
<span data-ttu-id="4cced-110">Especifica o nome da conta de automação com a conexão.</span><span class="sxs-lookup"><span data-stu-id="4cced-110">Specifies the name of the Automation account with the connection.</span></span>

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

### <span data-ttu-id="4cced-111">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="4cced-111">-ConnectionFieldName</span></span>
<span data-ttu-id="4cced-112">Especifica um nome para o campo.</span><span class="sxs-lookup"><span data-stu-id="4cced-112">Specifies a name for the field.</span></span>

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

### <span data-ttu-id="4cced-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="4cced-113">-Name</span></span>
<span data-ttu-id="4cced-114">Especifica um nome para a conexão.</span><span class="sxs-lookup"><span data-stu-id="4cced-114">Specifies a name for the connection.</span></span>

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

### <span data-ttu-id="4cced-115">-Perfil</span><span class="sxs-lookup"><span data-stu-id="4cced-115">-Profile</span></span>
<span data-ttu-id="4cced-116">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="4cced-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4cced-117">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="4cced-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4cced-118">-Valor</span><span class="sxs-lookup"><span data-stu-id="4cced-118">-Value</span></span>
<span data-ttu-id="4cced-119">Especifica um valor a ser armazenado no campo de conexão.</span><span class="sxs-lookup"><span data-stu-id="4cced-119">Specifies a value to store in the connection field.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cced-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cced-120">CommonParameters</span></span>
<span data-ttu-id="4cced-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cced-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cced-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cced-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cced-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4cced-123">INPUTS</span></span>

## <span data-ttu-id="4cced-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4cced-124">OUTPUTS</span></span>

## <span data-ttu-id="4cced-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4cced-125">NOTES</span></span>

## <span data-ttu-id="4cced-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4cced-126">RELATED LINKS</span></span>

[<span data-ttu-id="4cced-127">Get-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="4cced-127">Get-AzureAutomationConnection</span></span>](./Get-AzureAutomationConnection.md)

[<span data-ttu-id="4cced-128">New-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="4cced-128">New-AzureAutomationConnection</span></span>](./New-AzureAutomationConnection.md)

[<span data-ttu-id="4cced-129">Remove-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="4cced-129">Remove-AzureAutomationConnection</span></span>](./Remove-AzureAutomationConnection.md)


