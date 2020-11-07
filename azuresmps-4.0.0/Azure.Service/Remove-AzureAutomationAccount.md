---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: B8E4F6BD-FBF2-4B19-AA61-02149F933ABB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 52cba1ea3d42640693f2f330bf158a1eb078eebc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946495"
---
# <span data-ttu-id="36443-101">Remove-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="36443-101">Remove-AzureAutomationAccount</span></span>

## <span data-ttu-id="36443-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="36443-102">SYNOPSIS</span></span>

<span data-ttu-id="36443-103">Remove uma conta de automação.</span><span class="sxs-lookup"><span data-stu-id="36443-103">Removes an Automation Account.</span></span>

## <span data-ttu-id="36443-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36443-104">SYNTAX</span></span>

```
Remove-AzureAutomationAccount -Name <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="36443-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="36443-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="36443-106">O cmdlet **Remove-AzureAutomationAccount** remove uma conta da automação do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="36443-106">The **Remove-AzureAutomationAccount** cmdlet removes an account from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="36443-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="36443-107">EXAMPLES</span></span>

### <span data-ttu-id="36443-108">Exemplo 1: remover uma conta de automação</span><span class="sxs-lookup"><span data-stu-id="36443-108">Example 1: Remove an Automation account</span></span>
```
PS C:\> Remove-AzureAutomationAccount -Name "MyAutomationAccount" -Force
```

<span data-ttu-id="36443-109">Esse comando Remove uma conta de automação chamada MyAutomationAccount sem solicitar a validação do usuário.</span><span class="sxs-lookup"><span data-stu-id="36443-109">This command removes an Automation account named MyAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="36443-110">OS</span><span class="sxs-lookup"><span data-stu-id="36443-110">PARAMETERS</span></span>

### <span data-ttu-id="36443-111">-Force</span><span class="sxs-lookup"><span data-stu-id="36443-111">-Force</span></span>
<span data-ttu-id="36443-112">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="36443-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="36443-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="36443-113">-Name</span></span>
<span data-ttu-id="36443-114">Especifica o nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="36443-114">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="36443-115">-Perfil</span><span class="sxs-lookup"><span data-stu-id="36443-115">-Profile</span></span>
<span data-ttu-id="36443-116">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="36443-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="36443-117">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="36443-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="36443-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36443-118">CommonParameters</span></span>
<span data-ttu-id="36443-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36443-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36443-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36443-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36443-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="36443-121">INPUTS</span></span>

## <span data-ttu-id="36443-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="36443-122">OUTPUTS</span></span>

## <span data-ttu-id="36443-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="36443-123">NOTES</span></span>

## <span data-ttu-id="36443-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="36443-124">RELATED LINKS</span></span>

[<span data-ttu-id="36443-125">Get-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="36443-125">Get-AzureAutomationAccount</span></span>](./Get-AzureAutomationAccount.md)

[<span data-ttu-id="36443-126">New-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="36443-126">New-AzureAutomationAccount</span></span>](./New-AzureAutomationAccount.md)


