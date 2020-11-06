---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: f3afbd9b96de51f754dd87dfa42ed6f71e5b3577
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93425484"
---
# <span data-ttu-id="f344d-101">Save-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="f344d-101">Save-AzureRmContext</span></span>

## <span data-ttu-id="f344d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f344d-102">SYNOPSIS</span></span>
<span data-ttu-id="f344d-103">Salva as informações de autenticação atuais para usar em outras sessões do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f344d-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="f344d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f344d-104">SYNTAX</span></span>

```
Save-AzureRmContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="f344d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f344d-105">DESCRIPTION</span></span>
<span data-ttu-id="f344d-106">O cmdlet Save-AzureRmContext salva as informações de autenticação atuais para uso em outras sessões do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f344d-106">The Save-AzureRmContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="f344d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f344d-107">EXAMPLES</span></span>

### <span data-ttu-id="f344d-108">Exemplo 1: salvando o contexto da sessão atual</span><span class="sxs-lookup"><span data-stu-id="f344d-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmContext -Path C:\test.json
```

<span data-ttu-id="f344d-109">Este exemplo salva o contexto do Azure da sessão atual no arquivo JSON fornecido.</span><span class="sxs-lookup"><span data-stu-id="f344d-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="f344d-110">Exemplo 2: salvando um determinado contexto</span><span class="sxs-lookup"><span data-stu-id="f344d-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzureRmContext -Profile (Add-AzureRmAccount) -Path C:\test.json
```

<span data-ttu-id="f344d-111">Este exemplo salva o contexto do Azure que é passado para o cmdlet para o arquivo JSON fornecido.</span><span class="sxs-lookup"><span data-stu-id="f344d-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="f344d-112">OS</span><span class="sxs-lookup"><span data-stu-id="f344d-112">PARAMETERS</span></span>

### <span data-ttu-id="f344d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f344d-113">-Force</span></span>
<span data-ttu-id="f344d-114">Substituir o arquivo fornecido se ele existir</span><span class="sxs-lookup"><span data-stu-id="f344d-114">Overwrite the given file if it exists</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f344d-115">-Caminho</span><span class="sxs-lookup"><span data-stu-id="f344d-115">-Path</span></span>
<span data-ttu-id="f344d-116">Especifica o caminho do arquivo no qual as informações de autenticação são salvas.</span><span class="sxs-lookup"><span data-stu-id="f344d-116">Specifies the path of the file to which to save authentication information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f344d-117">-Perfil</span><span class="sxs-lookup"><span data-stu-id="f344d-117">-Profile</span></span>
<span data-ttu-id="f344d-118">Especifica o contexto do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="f344d-118">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="f344d-119">Se você não especificar um contexto, esse cmdlet lerá do contexto padrão local.</span><span class="sxs-lookup"><span data-stu-id="f344d-119">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: AzureRmProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f344d-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f344d-120">-Confirm</span></span>
<span data-ttu-id="f344d-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f344d-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f344d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f344d-122">-WhatIf</span></span>
<span data-ttu-id="f344d-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f344d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f344d-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f344d-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="f344d-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f344d-125">INPUTS</span></span>

### <span data-ttu-id="f344d-126">Microsoft. Azure. Commands. Common. Authentication. Models. AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="f344d-126">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRMProfile</span></span>

## <span data-ttu-id="f344d-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f344d-127">OUTPUTS</span></span>

### <span data-ttu-id="f344d-128">Microsoft. Azure. Commands. Profile. Models. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="f344d-128">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="f344d-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f344d-129">NOTES</span></span>

## <span data-ttu-id="f344d-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f344d-130">RELATED LINKS</span></span>

