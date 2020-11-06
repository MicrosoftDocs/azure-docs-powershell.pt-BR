---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/import-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Import-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Import-AzureRmContext.md
ms.openlocfilehash: 590557d883979ac3f23decd88695695df9aecc0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430092"
---
# <span data-ttu-id="60742-101">Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="60742-101">Import-AzureRmContext</span></span>

## <span data-ttu-id="60742-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="60742-102">SYNOPSIS</span></span>
<span data-ttu-id="60742-103">Carrega as informações de autenticação do Azure de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="60742-103">Loads Azure authentication information from a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60742-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="60742-104">SYNTAX</span></span>

### <span data-ttu-id="60742-105">ProfileFromDisk (padrão)</span><span class="sxs-lookup"><span data-stu-id="60742-105">ProfileFromDisk (Default)</span></span>
```
Import-AzureRmContext [-Path] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60742-106">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="60742-106">InMemoryProfile</span></span>
```
Import-AzureRmContext [-AzureContext] <AzureRmProfile> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60742-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="60742-107">DESCRIPTION</span></span>
<span data-ttu-id="60742-108">O cmdlet Import-AzureRmContext carrega informações de autenticação de um arquivo para definir o contexto e o ambiente do Azure.</span><span class="sxs-lookup"><span data-stu-id="60742-108">The Import-AzureRmContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="60742-109">Cmdlets que você executa na sessão atual usam essas informações para autenticar solicitações ao Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="60742-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="60742-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="60742-110">EXAMPLES</span></span>

### <span data-ttu-id="60742-111">Exemplo 1: importando um contexto de um AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="60742-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzureRmContext -AzureContext (Connect-AzureRmAccount)

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="60742-112">Este exemplo importa um contexto de um PSAzureProfile que é passado para o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60742-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="60742-113">Exemplo 2: importar um contexto de um arquivo JSON</span><span class="sxs-lookup"><span data-stu-id="60742-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzureRmContext -Path C:\test.json

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="60742-114">Este exemplo seleciona um contexto de um arquivo JSON que é passado pelo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60742-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="60742-115">Esse arquivo JSON pode ser criado a partir de Save-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="60742-115">This JSON file can be created from Save-AzureRmContext.</span></span>

## <span data-ttu-id="60742-116">OS</span><span class="sxs-lookup"><span data-stu-id="60742-116">PARAMETERS</span></span>

### <span data-ttu-id="60742-117">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="60742-117">-AzureContext</span></span>
<span data-ttu-id="60742-118">Especifica o contexto do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="60742-118">Specifies the Azure context from which this cmdlet reads.</span></span> <span data-ttu-id="60742-119">Se você não especificar um contexto, esse cmdlet lerá do contexto padrão local.</span><span class="sxs-lookup"><span data-stu-id="60742-119">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile
Parameter Sets: InMemoryProfile
Aliases: Profile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60742-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60742-120">-DefaultProfile</span></span>
<span data-ttu-id="60742-121">As credenciais, o locatário e a assinatura usados para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="60742-121">The credentials, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60742-122">-Caminho</span><span class="sxs-lookup"><span data-stu-id="60742-122">-Path</span></span>
<span data-ttu-id="60742-123">Especifica o caminho para as informações de contexto salvas usando Save-AzureRMContext.</span><span class="sxs-lookup"><span data-stu-id="60742-123">Specifies the path to context information saved by using Save-AzureRMContext.</span></span>

```yaml
Type: System.String
Parameter Sets: ProfileFromDisk
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60742-124">-Escopo</span><span class="sxs-lookup"><span data-stu-id="60742-124">-Scope</span></span>
<span data-ttu-id="60742-125">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam somente ao processo atual ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="60742-125">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60742-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="60742-126">-Confirm</span></span>
<span data-ttu-id="60742-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60742-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60742-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60742-128">-WhatIf</span></span>
<span data-ttu-id="60742-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="60742-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60742-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="60742-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60742-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60742-131">CommonParameters</span></span>
<span data-ttu-id="60742-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60742-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60742-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60742-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60742-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="60742-134">INPUTS</span></span>

### <span data-ttu-id="60742-135">Microsoft. Azure. Commands. Common. Authentication. Models. AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="60742-135">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

### <span data-ttu-id="60742-136">System. String</span><span class="sxs-lookup"><span data-stu-id="60742-136">System.String</span></span>

## <span data-ttu-id="60742-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="60742-137">OUTPUTS</span></span>

### <span data-ttu-id="60742-138">Microsoft. Azure. Commands. Profile. Models. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="60742-138">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="60742-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="60742-139">NOTES</span></span>

## <span data-ttu-id="60742-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="60742-140">RELATED LINKS</span></span>
