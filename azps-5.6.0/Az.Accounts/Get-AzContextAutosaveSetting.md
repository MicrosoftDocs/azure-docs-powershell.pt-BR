---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-azcontextautosavesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
ms.openlocfilehash: 629e35c5b700477fc46565b2da0e5dcf6f3c5b6f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889054"
---
# <span data-ttu-id="795b2-101">Get-AzContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="795b2-101">Get-AzContextAutosaveSetting</span></span>

## <span data-ttu-id="795b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="795b2-102">SYNOPSIS</span></span>
<span data-ttu-id="795b2-103">Exibe metadados sobre o recurso de autosave de contexto, incluindo se o contexto é salvo automaticamente e onde as informações de contexto e credencial salvas podem ser encontradas.</span><span class="sxs-lookup"><span data-stu-id="795b2-103">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="795b2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="795b2-104">SYNTAX</span></span>

```
Get-AzContextAutosaveSetting [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="795b2-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="795b2-105">DESCRIPTION</span></span>
<span data-ttu-id="795b2-106">Exibe metadados sobre o recurso de autosave de contexto, incluindo se o contexto é salvo automaticamente e onde as informações de contexto e credencial salvas podem ser encontradas.</span><span class="sxs-lookup"><span data-stu-id="795b2-106">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="795b2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="795b2-107">EXAMPLES</span></span>

### <span data-ttu-id="795b2-108">Obter metadados de salvar contexto para a sessão atual</span><span class="sxs-lookup"><span data-stu-id="795b2-108">Get context save metadata for the current session</span></span>
```
PS C:\> Get-AzContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

<span data-ttu-id="795b2-109">Obter detalhes sobre se e onde o contexto é salvo.</span><span class="sxs-lookup"><span data-stu-id="795b2-109">Get details about whether and where the context is saved.</span></span>  <span data-ttu-id="795b2-110">No exemplo acima, o recurso de autosave foi desabilitado.</span><span class="sxs-lookup"><span data-stu-id="795b2-110">In the above example, the autosave feature has been disabled.</span></span>

### <span data-ttu-id="795b2-111">Obter metadados de salvar contexto para o usuário atual</span><span class="sxs-lookup"><span data-stu-id="795b2-111">Get context save metadata for the current user</span></span>
```
PS C:\> Get-AzContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

<span data-ttu-id="795b2-112">Obter detalhes sobre se e onde o contexto é salvo por padrão para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="795b2-112">Get details about whether and where the context is saved by default for the current user.</span></span>  <span data-ttu-id="795b2-113">Observe que isso pode ser diferente das configurações que estão ativas na sessão atual.</span><span class="sxs-lookup"><span data-stu-id="795b2-113">Note that this may be different than the settings that are active in the current session.</span></span> <span data-ttu-id="795b2-114">No exemplo acima, o recurso de autosave foi habilitado e os dados são salvos no local padrão.</span><span class="sxs-lookup"><span data-stu-id="795b2-114">In the above example, the autosave feature has been enabled, and data is saved to the default location.</span></span>

## <span data-ttu-id="795b2-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="795b2-115">PARAMETERS</span></span>

### <span data-ttu-id="795b2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="795b2-116">-DefaultProfile</span></span>
<span data-ttu-id="795b2-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="795b2-117">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="795b2-118">-Scope</span><span class="sxs-lookup"><span data-stu-id="795b2-118">-Scope</span></span>
<span data-ttu-id="795b2-119">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam apenas ao processo atual ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="795b2-119">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="795b2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="795b2-120">CommonParameters</span></span>
<span data-ttu-id="795b2-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="795b2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="795b2-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="795b2-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="795b2-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="795b2-123">INPUTS</span></span>

### <span data-ttu-id="795b2-124">Nenhum</span><span class="sxs-lookup"><span data-stu-id="795b2-124">None</span></span>

## <span data-ttu-id="795b2-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="795b2-125">OUTPUTS</span></span>

### <span data-ttu-id="795b2-126">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="795b2-126">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="795b2-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="795b2-127">NOTES</span></span>

## <span data-ttu-id="795b2-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="795b2-128">RELATED LINKS</span></span>
