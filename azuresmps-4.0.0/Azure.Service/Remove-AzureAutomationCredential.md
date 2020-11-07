---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 4D87DD30-4AEF-4269-93B2-AE5964334AC8
online version: ''
schema: 2.0.0
ms.openlocfilehash: b581712f020b8168c052634e0f20244e16a7d950
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946480"
---
# <span data-ttu-id="737fa-101">Remove-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="737fa-101">Remove-AzureAutomationCredential</span></span>

## <span data-ttu-id="737fa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="737fa-102">SYNOPSIS</span></span>

<span data-ttu-id="737fa-103">Remove uma credencial da automação.</span><span class="sxs-lookup"><span data-stu-id="737fa-103">Removes a credential from Automation.</span></span>

## <span data-ttu-id="737fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="737fa-104">SYNTAX</span></span>

```
Remove-AzureAutomationCredential -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="737fa-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="737fa-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="737fa-106">O cmdlet **Remove-AzureAutomationCredential** remove uma credencial da automação do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="737fa-106">The **Remove-AzureAutomationCredential** cmdlet removes a credential from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="737fa-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="737fa-107">EXAMPLES</span></span>

### <span data-ttu-id="737fa-108">Exemplo 1: remover uma credencial</span><span class="sxs-lookup"><span data-stu-id="737fa-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzureAutomationCredential -AutomationAccountName "Contoso17" -Name "MyCredential"
```

<span data-ttu-id="737fa-109">Esse comando Remove uma credencial chamada mycredential na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="737fa-109">This command removes a credential named MyCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="737fa-110">OS</span><span class="sxs-lookup"><span data-stu-id="737fa-110">PARAMETERS</span></span>

### <span data-ttu-id="737fa-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="737fa-111">-AutomationAccountName</span></span>
<span data-ttu-id="737fa-112">Especifica o nome da conta de automação com a credencial.</span><span class="sxs-lookup"><span data-stu-id="737fa-112">Specifies the name of the Automation account with the credential.</span></span>

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

### <span data-ttu-id="737fa-113">-Force</span><span class="sxs-lookup"><span data-stu-id="737fa-113">-Force</span></span>
<span data-ttu-id="737fa-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="737fa-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="737fa-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="737fa-115">-Name</span></span>
<span data-ttu-id="737fa-116">Especifica o nome da credencial a ser removida.</span><span class="sxs-lookup"><span data-stu-id="737fa-116">Specifies the name of the credential to remove.</span></span>

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

### <span data-ttu-id="737fa-117">-Perfil</span><span class="sxs-lookup"><span data-stu-id="737fa-117">-Profile</span></span>
<span data-ttu-id="737fa-118">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="737fa-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="737fa-119">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="737fa-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="737fa-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="737fa-120">CommonParameters</span></span>
<span data-ttu-id="737fa-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="737fa-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="737fa-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="737fa-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="737fa-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="737fa-123">INPUTS</span></span>

## <span data-ttu-id="737fa-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="737fa-124">OUTPUTS</span></span>

## <span data-ttu-id="737fa-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="737fa-125">NOTES</span></span>

## <span data-ttu-id="737fa-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="737fa-126">RELATED LINKS</span></span>

[<span data-ttu-id="737fa-127">Get-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="737fa-127">Get-AzureAutomationCredential</span></span>](./Get-AzureAutomationCredential.md)

[<span data-ttu-id="737fa-128">New-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="737fa-128">New-AzureAutomationCredential</span></span>](./New-AzureAutomationCredential.md)

[<span data-ttu-id="737fa-129">Set-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="737fa-129">Set-AzureAutomationCredential</span></span>](./Set-AzureAutomationCredential.md)


