---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontextautosavesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
ms.openlocfilehash: a6361fabaa05d99b35874ce0de388ed0fc1bdfa7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595801"
---
# <span data-ttu-id="1c1b7-101">Get-AzContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="1c1b7-101">Get-AzContextAutosaveSetting</span></span>

## <span data-ttu-id="1c1b7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1c1b7-102">SYNOPSIS</span></span>
<span data-ttu-id="1c1b7-103">Exiba metadados sobre o recurso de salvamento automático de contexto, incluindo se o contexto é salvo automaticamente e onde as informações de contexto e credenciais salvas podem ser encontradas.</span><span class="sxs-lookup"><span data-stu-id="1c1b7-103">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="1c1b7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1c1b7-104">SYNTAX</span></span>

```
Get-AzContextAutosaveSetting [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1c1b7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1c1b7-105">DESCRIPTION</span></span>
<span data-ttu-id="1c1b7-106">Exiba metadados sobre o recurso de salvamento automático de contexto, incluindo se o contexto é salvo automaticamente e onde as informações de contexto e credenciais salvas podem ser encontradas.</span><span class="sxs-lookup"><span data-stu-id="1c1b7-106">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="1c1b7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1c1b7-107">EXAMPLES</span></span>

### <span data-ttu-id="1c1b7-108">Obter metadados de salvamento de contexto para a sessão atual</span><span class="sxs-lookup"><span data-stu-id="1c1b7-108">Get context save metadata for the current session</span></span>
```
PS C:\> Get-AzContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

<span data-ttu-id="1c1b7-109">Obter detalhes sobre se e WEHERE o contexto foi salvo.</span><span class="sxs-lookup"><span data-stu-id="1c1b7-109">Get details about whether and wehere the context is saved.</span></span>  <span data-ttu-id="1c1b7-110">No exemplo acima, o recurso salvamento automático foi desabilitado.</span><span class="sxs-lookup"><span data-stu-id="1c1b7-110">In the above example, the autosave feature has been disabled.</span></span>

### <span data-ttu-id="1c1b7-111">Obter metadados de salvamento de contexto para o usuário atual</span><span class="sxs-lookup"><span data-stu-id="1c1b7-111">Get context save metadata for the current user</span></span>
```
PS C:\> Get-AzContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

<span data-ttu-id="1c1b7-112">Obter detalhes sobre se e WEHERE o contexto é salvo por padrão para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="1c1b7-112">Get details about whether and wehere the context is saved by default for the current user.</span></span>  <span data-ttu-id="1c1b7-113">Observe que isso pode ser diferente das configurações ativas na sessão atual.</span><span class="sxs-lookup"><span data-stu-id="1c1b7-113">Note that this may be different than the settings that are active in the current session.</span></span> <span data-ttu-id="1c1b7-114">No exemplo acima, o recurso salvamento automático foi habilitado e os dados são salvos no local padrão.</span><span class="sxs-lookup"><span data-stu-id="1c1b7-114">In the above example, the autosave feature has been enabled, and data is saved to the default location.</span></span>

## <span data-ttu-id="1c1b7-115">OS</span><span class="sxs-lookup"><span data-stu-id="1c1b7-115">PARAMETERS</span></span>

### <span data-ttu-id="1c1b7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c1b7-116">-DefaultProfile</span></span>
<span data-ttu-id="1c1b7-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1c1b7-117">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c1b7-118">-Escopo</span><span class="sxs-lookup"><span data-stu-id="1c1b7-118">-Scope</span></span>
<span data-ttu-id="1c1b7-119">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam somente ao processo atual ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="1c1b7-119">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="1c1b7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c1b7-120">CommonParameters</span></span>
<span data-ttu-id="1c1b7-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c1b7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c1b7-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c1b7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c1b7-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1c1b7-123">INPUTS</span></span>

### <span data-ttu-id="1c1b7-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1c1b7-124">None</span></span>

## <span data-ttu-id="1c1b7-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1c1b7-125">OUTPUTS</span></span>

### <span data-ttu-id="1c1b7-126">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="1c1b7-126">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="1c1b7-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1c1b7-127">NOTES</span></span>

## <span data-ttu-id="1c1b7-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1c1b7-128">RELATED LINKS</span></span>
