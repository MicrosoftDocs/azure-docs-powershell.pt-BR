---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/import-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Import-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Import-AzContext.md
ms.openlocfilehash: 02f1eeb648ae379e1cb1ec0cf90bb98307fd97ac
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775248"
---
# <span data-ttu-id="a9218-101">Import-AzContext</span><span class="sxs-lookup"><span data-stu-id="a9218-101">Import-AzContext</span></span>

## <span data-ttu-id="a9218-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a9218-102">SYNOPSIS</span></span>
<span data-ttu-id="a9218-103">Carrega as informações de autenticação do Azure de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="a9218-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="a9218-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9218-104">SYNTAX</span></span>

### <span data-ttu-id="a9218-105">ProfileFromDisk (padrão)</span><span class="sxs-lookup"><span data-stu-id="a9218-105">ProfileFromDisk (Default)</span></span>
```
Import-AzContext [-Path] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9218-106">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="a9218-106">InMemoryProfile</span></span>
```
Import-AzContext [-AzureContext] <AzureRmProfile> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9218-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a9218-107">DESCRIPTION</span></span>
<span data-ttu-id="a9218-108">O cmdlet Import-AzContext carrega informações de autenticação de um arquivo para definir o contexto e o ambiente do Azure.</span><span class="sxs-lookup"><span data-stu-id="a9218-108">The Import-AzContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="a9218-109">Cmdlets que você executa na sessão atual usam essas informações para autenticar solicitações ao Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="a9218-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="a9218-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a9218-110">EXAMPLES</span></span>

### <span data-ttu-id="a9218-111">Exemplo 1: importando um contexto de um AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="a9218-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzContext -AzContext (Connect-AzAccount)

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="a9218-112">Este exemplo importa um contexto de um PSAzureProfile que é passado para o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9218-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="a9218-113">Exemplo 2: importar um contexto de um arquivo JSON</span><span class="sxs-lookup"><span data-stu-id="a9218-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzContext -Path C:\test.json

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="a9218-114">Este exemplo seleciona um contexto de um arquivo JSON que é passado pelo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9218-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="a9218-115">Esse arquivo JSON pode ser criado a partir de Save-AzContext.</span><span class="sxs-lookup"><span data-stu-id="a9218-115">This JSON file can be created from Save-AzContext.</span></span>

## <span data-ttu-id="a9218-116">OS</span><span class="sxs-lookup"><span data-stu-id="a9218-116">PARAMETERS</span></span>

### <span data-ttu-id="a9218-117">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="a9218-117">-AzureContext</span></span>
<span data-ttu-id="a9218-118">{{Fill AzureContext descrição}}</span><span class="sxs-lookup"><span data-stu-id="a9218-118">{{Fill AzureContext Description}}</span></span>

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

### <span data-ttu-id="a9218-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9218-119">-DefaultProfile</span></span>
<span data-ttu-id="a9218-120">As credenciais, o locatário e a assinatura usados para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a9218-120">The credentials, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9218-121">-Caminho</span><span class="sxs-lookup"><span data-stu-id="a9218-121">-Path</span></span>
<span data-ttu-id="a9218-122">Especifica o caminho para as informações de contexto salvas usando Save-AzContext.</span><span class="sxs-lookup"><span data-stu-id="a9218-122">Specifies the path to context information saved by using Save-AzContext.</span></span>

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

### <span data-ttu-id="a9218-123">-Escopo</span><span class="sxs-lookup"><span data-stu-id="a9218-123">-Scope</span></span>
<span data-ttu-id="a9218-124">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam somente ao processo atual ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="a9218-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="a9218-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a9218-125">-Confirm</span></span>
<span data-ttu-id="a9218-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9218-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9218-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9218-127">-WhatIf</span></span>
<span data-ttu-id="a9218-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a9218-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9218-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a9218-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9218-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9218-130">CommonParameters</span></span>
<span data-ttu-id="a9218-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9218-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9218-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9218-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9218-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a9218-133">INPUTS</span></span>

### <span data-ttu-id="a9218-134">Microsoft. Azure. Commands. Common. Authentication. Models. AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="a9218-134">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

### <span data-ttu-id="a9218-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a9218-135">System.String</span></span>

## <span data-ttu-id="a9218-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a9218-136">OUTPUTS</span></span>

### <span data-ttu-id="a9218-137">Microsoft. Azure. Commands. Profile. Models. Core. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="a9218-137">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="a9218-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a9218-138">NOTES</span></span>

## <span data-ttu-id="a9218-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a9218-139">RELATED LINKS</span></span>