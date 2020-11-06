---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 46efba5e2ab9a5c51172264b343b0f4f2b508065
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93425483"
---
# <span data-ttu-id="324f6-101">Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="324f6-101">Import-AzureRmContext</span></span>

## <span data-ttu-id="324f6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="324f6-102">SYNOPSIS</span></span>
<span data-ttu-id="324f6-103">Carrega as informações de autenticação do Azure de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="324f6-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="324f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="324f6-104">SYNTAX</span></span>

### <span data-ttu-id="324f6-105">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="324f6-105">InMemoryProfile</span></span>
```
Import-AzureRmContext [-AzureContext] <AzureRmProfile> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="324f6-106">ProfileFromDisk</span><span class="sxs-lookup"><span data-stu-id="324f6-106">ProfileFromDisk</span></span>
```
Import-AzureRmContext [-Path] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="324f6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="324f6-107">DESCRIPTION</span></span>
<span data-ttu-id="324f6-108">O cmdlet Import-AzureRmContext carrega informações de autenticação de um arquivo para definir o contexto e o ambiente do Azure.</span><span class="sxs-lookup"><span data-stu-id="324f6-108">The Import-AzureRmContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="324f6-109">Cmdlets que você executa na sessão atual usam essas informações para autenticar solicitações ao Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="324f6-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="324f6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="324f6-110">EXAMPLES</span></span>

### <span data-ttu-id="324f6-111">Exemplo 1: importando um contexto de um AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="324f6-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzureRmContext -AzureContext (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="324f6-112">Este exemplo importa um contexto de um PSAzureProfile que é passado para o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="324f6-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="324f6-113">Exemplo 2: importar um contexto de um arquivo JSON</span><span class="sxs-lookup"><span data-stu-id="324f6-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzureRmContext -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="324f6-114">Este exemplo seleciona um contexto de um arquivo JSON que é passado pelo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="324f6-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span>
<span data-ttu-id="324f6-115">Esse arquivo JSON pode ser criado a partir de Import-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="324f6-115">This JSON file can be created from Import-AzureRmContext.</span></span>

## <span data-ttu-id="324f6-116">OS</span><span class="sxs-lookup"><span data-stu-id="324f6-116">PARAMETERS</span></span>

### <span data-ttu-id="324f6-117">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="324f6-117">-AzureContext</span></span>
<span data-ttu-id="324f6-118">Especifica o contexto do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="324f6-118">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="324f6-119">Se você não especificar um contexto, esse cmdlet lerá do contexto padrão local.</span><span class="sxs-lookup"><span data-stu-id="324f6-119">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: AzureRmProfile
Parameter Sets: InMemoryProfile
Aliases: Profile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="324f6-120">-Caminho</span><span class="sxs-lookup"><span data-stu-id="324f6-120">-Path</span></span>
<span data-ttu-id="324f6-121">Especifica o caminho para as informações de contexto salvas usando Save-AzureRMContext.</span><span class="sxs-lookup"><span data-stu-id="324f6-121">Specifies the path to context information saved by using Save-AzureRMContext.</span></span>

```yaml
Type: String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="324f6-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="324f6-122">-Confirm</span></span>
<span data-ttu-id="324f6-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="324f6-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="324f6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="324f6-124">-WhatIf</span></span>
<span data-ttu-id="324f6-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="324f6-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="324f6-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="324f6-126">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="324f6-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="324f6-127">INPUTS</span></span>

### <span data-ttu-id="324f6-128">Microsoft. Azure. Commands. Common. Authentication. Models. AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="324f6-128">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRMProfile</span></span>
<span data-ttu-id="324f6-129">System. String</span><span class="sxs-lookup"><span data-stu-id="324f6-129">System.String</span></span>

## <span data-ttu-id="324f6-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="324f6-130">OUTPUTS</span></span>

### <span data-ttu-id="324f6-131">Microsoft. Azure. Commands. Profile. Models. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="324f6-131">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="324f6-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="324f6-132">NOTES</span></span>

## <span data-ttu-id="324f6-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="324f6-133">RELATED LINKS</span></span>

