---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 9CED6E53-B65C-4D55-8AC7-9E8A8B143544
online version: ''
schema: 2.0.0
ms.openlocfilehash: da8f0e3bdc9e1cf573e9189e49feda85ee8c1b90
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945830"
---
# <span data-ttu-id="7349d-101">Set-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="7349d-101">Set-AzureAutomationModule</span></span>

## <span data-ttu-id="7349d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7349d-102">SYNOPSIS</span></span>

<span data-ttu-id="7349d-103">Atualiza um módulo na automação.</span><span class="sxs-lookup"><span data-stu-id="7349d-103">Updates a module in Automation.</span></span>

## <span data-ttu-id="7349d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7349d-104">SYNTAX</span></span>

```
Set-AzureAutomationModule -Name <String> [-Tags <IDictionary>] [-ContentLinkUri <Uri>]
 [-ContentLinkVersion <String>] -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="7349d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7349d-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="7349d-106">O cmdlet **set-AzureAutomationModule** importa uma nova versão de um módulo ou altera a configuração do módulo na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="7349d-106">The **Set-AzureAutomationModule** cmdlet imports a new version of a module or changes the configuration of the module in Azure Automation.</span></span>

## <span data-ttu-id="7349d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7349d-107">EXAMPLES</span></span>

### <span data-ttu-id="7349d-108">Exemplo 1: atualizar um módulo</span><span class="sxs-lookup"><span data-stu-id="7349d-108">Example 1: Update a module</span></span>
```
PS C:\> Set-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri ".\ContosoModule.zip" -ContentLinkVersion "1.1"
```

<span data-ttu-id="7349d-109">Esse comando importa uma versão atualizada de um módulo existente chamado ContosoModule para a conta de automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7349d-109">This command imports an updated version of an existing module named ContosoModule into the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="7349d-110">OS</span><span class="sxs-lookup"><span data-stu-id="7349d-110">PARAMETERS</span></span>

### <span data-ttu-id="7349d-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7349d-111">-AutomationAccountName</span></span>
<span data-ttu-id="7349d-112">Especifica o nome da conta de automação com o módulo.</span><span class="sxs-lookup"><span data-stu-id="7349d-112">Specifies the name of the Automation account with the module.</span></span>

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

### <span data-ttu-id="7349d-113">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="7349d-113">-ContentLinkUri</span></span>
<span data-ttu-id="7349d-114">Especifica o caminho para o arquivo de módulo.</span><span class="sxs-lookup"><span data-stu-id="7349d-114">Specifies the path to the module file.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7349d-115">-ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="7349d-115">-ContentLinkVersion</span></span>
<span data-ttu-id="7349d-116">Especifica a versão do módulo.</span><span class="sxs-lookup"><span data-stu-id="7349d-116">Specifies the version of the module.</span></span>

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

### <span data-ttu-id="7349d-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="7349d-117">-Name</span></span>
<span data-ttu-id="7349d-118">Especifica o nome do módulo.</span><span class="sxs-lookup"><span data-stu-id="7349d-118">Specifies the name of the module.</span></span>

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

### <span data-ttu-id="7349d-119">-Perfil</span><span class="sxs-lookup"><span data-stu-id="7349d-119">-Profile</span></span>
<span data-ttu-id="7349d-120">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="7349d-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7349d-121">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="7349d-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7349d-122">-Marcas</span><span class="sxs-lookup"><span data-stu-id="7349d-122">-Tags</span></span>
<span data-ttu-id="7349d-123">Especifica as marcas do módulo.</span><span class="sxs-lookup"><span data-stu-id="7349d-123">Specifies tags for the module.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7349d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7349d-124">CommonParameters</span></span>
<span data-ttu-id="7349d-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7349d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7349d-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7349d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7349d-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7349d-127">INPUTS</span></span>

### <span data-ttu-id="7349d-128">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="7349d-128">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="7349d-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7349d-129">OUTPUTS</span></span>

## <span data-ttu-id="7349d-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7349d-130">NOTES</span></span>

## <span data-ttu-id="7349d-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7349d-131">RELATED LINKS</span></span>

[<span data-ttu-id="7349d-132">Get-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="7349d-132">Get-AzureAutomationModule</span></span>](./Get-AzureAutomationModule.md)

[<span data-ttu-id="7349d-133">New-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="7349d-133">New-AzureAutomationModule</span></span>](./New-AzureAutomationModule.md)

[<span data-ttu-id="7349d-134">Remove-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="7349d-134">Remove-AzureAutomationModule</span></span>](./Remove-AzureAutomationModule.md)


