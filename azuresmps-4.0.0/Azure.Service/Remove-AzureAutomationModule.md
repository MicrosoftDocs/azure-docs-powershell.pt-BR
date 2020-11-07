---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 73BE191D-816F-4376-8304-B0ABA4163EF6
online version: ''
schema: 2.0.0
ms.openlocfilehash: a75016368a770221fd0ab373a4b59c5975ee2a24
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946481"
---
# <span data-ttu-id="cad6f-101">Remove-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="cad6f-101">Remove-AzureAutomationModule</span></span>

## <span data-ttu-id="cad6f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cad6f-102">SYNOPSIS</span></span>

<span data-ttu-id="cad6f-103">Remove um módulo da automação.</span><span class="sxs-lookup"><span data-stu-id="cad6f-103">Removes a module from Automation.</span></span>

## <span data-ttu-id="cad6f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cad6f-104">SYNTAX</span></span>

```
Remove-AzureAutomationModule -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cad6f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cad6f-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="cad6f-106">O cmdlet **Remove-AzureAutomationModule** remove uma conta de automação da automação do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cad6f-106">The **Remove-AzureAutomationModule** cmdlet removes an Automation account from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="cad6f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cad6f-107">EXAMPLES</span></span>

### <span data-ttu-id="cad6f-108">Exemplo 1: remover um módulo</span><span class="sxs-lookup"><span data-stu-id="cad6f-108">Example 1: Remove a module</span></span>
```
PS C:\> Remove-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule"
```

<span data-ttu-id="cad6f-109">Esse comando Remove um módulo chamado ContosoModule da conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="cad6f-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="cad6f-110">OS</span><span class="sxs-lookup"><span data-stu-id="cad6f-110">PARAMETERS</span></span>

### <span data-ttu-id="cad6f-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cad6f-111">-AutomationAccountName</span></span>
<span data-ttu-id="cad6f-112">Especifica o nome da conta de automação com o módulo.</span><span class="sxs-lookup"><span data-stu-id="cad6f-112">Specifies the name of the Automation account with the module.</span></span>

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

### <span data-ttu-id="cad6f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="cad6f-113">-Force</span></span>
<span data-ttu-id="cad6f-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="cad6f-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cad6f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="cad6f-115">-Name</span></span>
<span data-ttu-id="cad6f-116">Especifica o nome do módulo a ser removido.</span><span class="sxs-lookup"><span data-stu-id="cad6f-116">Specifies the name of the module to remove.</span></span>

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

### <span data-ttu-id="cad6f-117">-Perfil</span><span class="sxs-lookup"><span data-stu-id="cad6f-117">-Profile</span></span>
<span data-ttu-id="cad6f-118">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="cad6f-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cad6f-119">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="cad6f-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cad6f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cad6f-120">CommonParameters</span></span>
<span data-ttu-id="cad6f-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cad6f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cad6f-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cad6f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cad6f-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cad6f-123">INPUTS</span></span>

## <span data-ttu-id="cad6f-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cad6f-124">OUTPUTS</span></span>

## <span data-ttu-id="cad6f-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cad6f-125">NOTES</span></span>

## <span data-ttu-id="cad6f-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cad6f-126">RELATED LINKS</span></span>

[<span data-ttu-id="cad6f-127">Get-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="cad6f-127">Get-AzureAutomationModule</span></span>](./Get-AzureAutomationModule.md)

[<span data-ttu-id="cad6f-128">New-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="cad6f-128">New-AzureAutomationModule</span></span>](./New-AzureAutomationModule.md)

[<span data-ttu-id="cad6f-129">Set-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="cad6f-129">Set-AzureAutomationModule</span></span>](./Set-AzureAutomationModule.md)


