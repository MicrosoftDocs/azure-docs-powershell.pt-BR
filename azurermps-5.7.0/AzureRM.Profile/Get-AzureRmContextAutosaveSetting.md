---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermcontextautosavesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContextAutosaveSetting.md
ms.openlocfilehash: d0d6c69bb85fcdf851f0f134bb376252525aec91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432440"
---
# <span data-ttu-id="955a1-101">Get-AzureRmContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="955a1-101">Get-AzureRmContextAutosaveSetting</span></span>

## <span data-ttu-id="955a1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="955a1-102">SYNOPSIS</span></span>
<span data-ttu-id="955a1-103">Exiba metadados sobre o recurso de salvamento automático de contexto, incluindo whterh o contexto é automaticamente Aved, e onde as informações de contexto e credenciais salvas podem ser encontradas.</span><span class="sxs-lookup"><span data-stu-id="955a1-103">Display metadata about the context autosave feature, including whterh the context is automaticallys aved, and where saved context and credential information cna be found.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="955a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="955a1-104">SYNTAX</span></span>

```
Get-AzureRmContextAutosaveSetting [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="955a1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="955a1-105">DESCRIPTION</span></span>
<span data-ttu-id="955a1-106">Exiba metadados sobre o recurso de salvamento automático de contexto, incluindo se o contexto é salvo automaticamente e onde as informações de contexto e credenciais salvas podem ser encontradas.</span><span class="sxs-lookup"><span data-stu-id="955a1-106">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="955a1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="955a1-107">EXAMPLES</span></span>

### <span data-ttu-id="955a1-108">Obter metadados de salvamento de contexto para a sessão atual</span><span class="sxs-lookup"><span data-stu-id="955a1-108">Get context save metadata for the current session</span></span>
```
PS C:\> Get-AzureRmContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

<span data-ttu-id="955a1-109">Obter detalhes sobre se e WEHERE o contexto foi salvo.</span><span class="sxs-lookup"><span data-stu-id="955a1-109">Get details about whether and wehere the context is saved.</span></span>  <span data-ttu-id="955a1-110">No exemplo acima, o recurso salvamento automático foi desabilitado.</span><span class="sxs-lookup"><span data-stu-id="955a1-110">In the above example, the autosave feature has been disabled.</span></span>

### <span data-ttu-id="955a1-111">Obter metadados de salvamento de contexto para o usuário atual</span><span class="sxs-lookup"><span data-stu-id="955a1-111">Get context save metadata for the current user</span></span>
```
PS C:\> Get-AzureRmContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

<span data-ttu-id="955a1-112">Obter detalhes sobre se e WEHERE o contexto é salvo por padrão para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="955a1-112">Get details about whether and wehere the context is saved by default for the current user.</span></span>  <span data-ttu-id="955a1-113">Observe que isso pode ser diferente das configurações ativas na sessão atual.</span><span class="sxs-lookup"><span data-stu-id="955a1-113">Note that this may be different than the settings that are active in the current session.</span></span> <span data-ttu-id="955a1-114">No exemplo acima, o recurso salvamento automático foi habilitado e os dados são salvos no local padrão.</span><span class="sxs-lookup"><span data-stu-id="955a1-114">In the above example, the autosave feature has been enabled, and data is saved to the default location.</span></span>

## <span data-ttu-id="955a1-115">OS</span><span class="sxs-lookup"><span data-stu-id="955a1-115">PARAMETERS</span></span>

### <span data-ttu-id="955a1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="955a1-116">-DefaultProfile</span></span>
<span data-ttu-id="955a1-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="955a1-117">The credentials, account, tenant and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="955a1-118">-Escopo</span><span class="sxs-lookup"><span data-stu-id="955a1-118">-Scope</span></span>
<span data-ttu-id="955a1-119">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam somente ao processo atual ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="955a1-119">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="955a1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="955a1-120">CommonParameters</span></span>
<span data-ttu-id="955a1-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="955a1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="955a1-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="955a1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="955a1-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="955a1-123">INPUTS</span></span>

### <span data-ttu-id="955a1-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="955a1-124">None</span></span>

## <span data-ttu-id="955a1-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="955a1-125">OUTPUTS</span></span>

### <span data-ttu-id="955a1-126">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="955a1-126">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>
<span data-ttu-id="955a1-127">Informações sobre as configurações atuais de salvamento automático, incluindo se o salvamento automático está habilitado para o usuário atual e onde os arquivos de contexto e credenciais são salvos.</span><span class="sxs-lookup"><span data-stu-id="955a1-127">Information about the current Autosave settings, including whether Autosave is enabled for the current user, and where context and credential files are saved.</span></span>

## <span data-ttu-id="955a1-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="955a1-128">NOTES</span></span>

## <span data-ttu-id="955a1-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="955a1-129">RELATED LINKS</span></span>
