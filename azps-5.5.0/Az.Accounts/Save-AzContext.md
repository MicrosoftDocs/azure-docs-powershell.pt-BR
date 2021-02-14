---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/save-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
ms.openlocfilehash: 2d3506fcf0968e58a71d81fbabe56f08428af761
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110861"
---
# <span data-ttu-id="acbe9-101">Save-AzContext</span><span class="sxs-lookup"><span data-stu-id="acbe9-101">Save-AzContext</span></span>

## <span data-ttu-id="acbe9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="acbe9-102">SYNOPSIS</span></span>
<span data-ttu-id="acbe9-103">Salva as informações de autenticação atuais para uso em outras sessões do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="acbe9-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="acbe9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="acbe9-104">SYNTAX</span></span>

```
Save-AzContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acbe9-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="acbe9-105">DESCRIPTION</span></span>
<span data-ttu-id="acbe9-106">O Save-AzContext cmdlet salva as informações de autenticação atuais para uso em outras sessões do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="acbe9-106">The Save-AzContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="acbe9-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="acbe9-107">EXAMPLES</span></span>

### <span data-ttu-id="acbe9-108">Exemplo 1: Salvando o contexto da sessão atual</span><span class="sxs-lookup"><span data-stu-id="acbe9-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Save-AzContext -Path C:\test.json
```

<span data-ttu-id="acbe9-109">Este exemplo salva o contexto do Azure da sessão atual no arquivo JSON fornecido.</span><span class="sxs-lookup"><span data-stu-id="acbe9-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="acbe9-110">Exemplo 2: Salvando um determinado contexto</span><span class="sxs-lookup"><span data-stu-id="acbe9-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzContext -Profile (Connect-AzAccount) -Path C:\test.json
```

<span data-ttu-id="acbe9-111">Este exemplo salva o contexto do Azure que é passado para o cmdlet para o arquivo JSON fornecido.</span><span class="sxs-lookup"><span data-stu-id="acbe9-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="acbe9-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="acbe9-112">PARAMETERS</span></span>

### <span data-ttu-id="acbe9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acbe9-113">-DefaultProfile</span></span>
<span data-ttu-id="acbe9-114">As credenciais, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="acbe9-114">The credentials, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acbe9-115">-Forçar</span><span class="sxs-lookup"><span data-stu-id="acbe9-115">-Force</span></span>
<span data-ttu-id="acbe9-116">Substituir o arquivo determinado se ele existir</span><span class="sxs-lookup"><span data-stu-id="acbe9-116">Overwrite the given file if it exists</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acbe9-117">-Caminho</span><span class="sxs-lookup"><span data-stu-id="acbe9-117">-Path</span></span>
<span data-ttu-id="acbe9-118">Especifica o caminho do arquivo para o qual as informações de autenticação são salvas.</span><span class="sxs-lookup"><span data-stu-id="acbe9-118">Specifies the path of the file to which to save authentication information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acbe9-119">-Perfil</span><span class="sxs-lookup"><span data-stu-id="acbe9-119">-Profile</span></span>
<span data-ttu-id="acbe9-120">Especifica o contexto do Azure a partir do qual este cmdlet é lido.</span><span class="sxs-lookup"><span data-stu-id="acbe9-120">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="acbe9-121">Se você não especificar um contexto, esse cmdlet será lido a partir do contexto padrão local.</span><span class="sxs-lookup"><span data-stu-id="acbe9-121">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="acbe9-122">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="acbe9-122">-Confirm</span></span>
<span data-ttu-id="acbe9-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="acbe9-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acbe9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acbe9-124">-WhatIf</span></span>
<span data-ttu-id="acbe9-125">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="acbe9-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acbe9-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="acbe9-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acbe9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acbe9-127">CommonParameters</span></span>
<span data-ttu-id="acbe9-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acbe9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acbe9-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acbe9-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acbe9-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="acbe9-130">INPUTS</span></span>

### <span data-ttu-id="acbe9-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="acbe9-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

## <span data-ttu-id="acbe9-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="acbe9-132">OUTPUTS</span></span>

### <span data-ttu-id="acbe9-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="acbe9-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="acbe9-134">Notas</span><span class="sxs-lookup"><span data-stu-id="acbe9-134">NOTES</span></span>

## <span data-ttu-id="acbe9-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="acbe9-135">RELATED LINKS</span></span>
