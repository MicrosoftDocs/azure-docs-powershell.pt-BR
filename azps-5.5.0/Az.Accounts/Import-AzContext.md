---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/import-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Import-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Import-AzContext.md
ms.openlocfilehash: 40d5cef72a8a1f345ac7f6389bacfb75257ccab4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114333"
---
# <span data-ttu-id="f55fe-101">Import-AzContext</span><span class="sxs-lookup"><span data-stu-id="f55fe-101">Import-AzContext</span></span>

## <span data-ttu-id="f55fe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f55fe-102">SYNOPSIS</span></span>
<span data-ttu-id="f55fe-103">Carrega informações de autenticação do Azure de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="f55fe-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="f55fe-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f55fe-104">SYNTAX</span></span>

### <span data-ttu-id="f55fe-105">ProfileFromDisk (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f55fe-105">ProfileFromDisk (Default)</span></span>
```
Import-AzContext [-Path] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f55fe-106">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="f55fe-106">InMemoryProfile</span></span>
```
Import-AzContext [-AzureContext] <AzureRmProfile> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f55fe-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f55fe-107">DESCRIPTION</span></span>
<span data-ttu-id="f55fe-108">O Import-AzContext cmdlet carrega informações de autenticação de um arquivo para definir o ambiente e o contexto do Azure.</span><span class="sxs-lookup"><span data-stu-id="f55fe-108">The Import-AzContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="f55fe-109">Os cmdlets executados na sessão atual usam essas informações para autenticar solicitações ao Gerenciador de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="f55fe-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="f55fe-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f55fe-110">EXAMPLES</span></span>

### <span data-ttu-id="f55fe-111">Exemplo 1: Importando um contexto de um AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="f55fe-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzContext -AzContext (Connect-AzAccount)

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="f55fe-112">Este exemplo importa um contexto de um PSAzureProfile que é passado para o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f55fe-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="f55fe-113">Exemplo 2: Importar um contexto de um arquivo JSON</span><span class="sxs-lookup"><span data-stu-id="f55fe-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzContext -Path C:\test.json

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="f55fe-114">Este exemplo seleciona um contexto de um arquivo JSON que é passado para o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f55fe-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="f55fe-115">Este arquivo JSON pode ser criado a partir do Save-AzContext.</span><span class="sxs-lookup"><span data-stu-id="f55fe-115">This JSON file can be created from Save-AzContext.</span></span>

## <span data-ttu-id="f55fe-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f55fe-116">PARAMETERS</span></span>

### <span data-ttu-id="f55fe-117">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="f55fe-117">-AzureContext</span></span>
<span data-ttu-id="f55fe-118">{{Fill AzureContext Description}}</span><span class="sxs-lookup"><span data-stu-id="f55fe-118">{{Fill AzureContext Description}}</span></span>

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

### <span data-ttu-id="f55fe-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f55fe-119">-DefaultProfile</span></span>
<span data-ttu-id="f55fe-120">As credenciais, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f55fe-120">The credentials, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f55fe-121">-Caminho</span><span class="sxs-lookup"><span data-stu-id="f55fe-121">-Path</span></span>
<span data-ttu-id="f55fe-122">Especifica o caminho para informações de contexto salvas usando Salvar-AzContext.</span><span class="sxs-lookup"><span data-stu-id="f55fe-122">Specifies the path to context information saved by using Save-AzContext.</span></span>

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

### <span data-ttu-id="f55fe-123">-Escopo</span><span class="sxs-lookup"><span data-stu-id="f55fe-123">-Scope</span></span>
<span data-ttu-id="f55fe-124">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam apenas ao processo atual ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="f55fe-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="f55fe-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f55fe-125">-Confirm</span></span>
<span data-ttu-id="f55fe-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f55fe-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f55fe-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f55fe-127">-WhatIf</span></span>
<span data-ttu-id="f55fe-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f55fe-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f55fe-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f55fe-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f55fe-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f55fe-130">CommonParameters</span></span>
<span data-ttu-id="f55fe-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f55fe-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f55fe-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f55fe-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f55fe-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="f55fe-133">INPUTS</span></span>

### <span data-ttu-id="f55fe-134">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="f55fe-134">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

### <span data-ttu-id="f55fe-135">System.String</span><span class="sxs-lookup"><span data-stu-id="f55fe-135">System.String</span></span>

## <span data-ttu-id="f55fe-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="f55fe-136">OUTPUTS</span></span>

### <span data-ttu-id="f55fe-137">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="f55fe-137">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="f55fe-138">Notas</span><span class="sxs-lookup"><span data-stu-id="f55fe-138">NOTES</span></span>

## <span data-ttu-id="f55fe-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f55fe-139">RELATED LINKS</span></span>
