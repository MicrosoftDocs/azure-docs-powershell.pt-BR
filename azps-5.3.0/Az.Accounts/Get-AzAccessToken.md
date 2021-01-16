---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azaccesstoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
ms.openlocfilehash: 696ae59cb5115181605b7e6e647e2eb7d2792fd8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98432833"
---
# <span data-ttu-id="d7229-101">Get-AzAccessToken</span><span class="sxs-lookup"><span data-stu-id="d7229-101">Get-AzAccessToken</span></span>

## <span data-ttu-id="d7229-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d7229-102">SYNOPSIS</span></span>
<span data-ttu-id="d7229-103">Obter token de acesso bruto.</span><span class="sxs-lookup"><span data-stu-id="d7229-103">Get raw access token.</span></span> <span data-ttu-id="d7229-104">Ao usar-ResourceUrl, certifique-se de que o valor corresponda ao ambiente atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="d7229-104">When using -ResourceUrl, please make sure the value does match current Azure environment.</span></span> <span data-ttu-id="d7229-105">Você pode se referir ao valor de `(Get-AzContext).Environment` .</span><span class="sxs-lookup"><span data-stu-id="d7229-105">You may refer to the value of `(Get-AzContext).Environment`.</span></span>

## <span data-ttu-id="d7229-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d7229-106">SYNTAX</span></span>

### <span data-ttu-id="d7229-107">KnownResourceTypeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="d7229-107">KnownResourceTypeName (Default)</span></span>
```
Get-AzAccessToken [-ResourceTypeName <String>] [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d7229-108">ResourceUrl</span><span class="sxs-lookup"><span data-stu-id="d7229-108">ResourceUrl</span></span>
```
Get-AzAccessToken -ResourceUrl <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d7229-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d7229-109">DESCRIPTION</span></span>
<span data-ttu-id="d7229-110">Obter token de acesso</span><span class="sxs-lookup"><span data-stu-id="d7229-110">Get access token</span></span>

## <span data-ttu-id="d7229-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d7229-111">EXAMPLES</span></span>

### <span data-ttu-id="d7229-112">Exemplo 1 obter token de acesso bruto para o ponto de extremidade do ARM</span><span class="sxs-lookup"><span data-stu-id="d7229-112">Example 1 Get raw access token for ARM endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken
```

<span data-ttu-id="d7229-113">Obter o token de acesso do ponto de extremidade ResourceManager para a conta atual</span><span class="sxs-lookup"><span data-stu-id="d7229-113">Get access token of ResourceManager endpoint for current account</span></span>

### <span data-ttu-id="d7229-114">Exemplo 2 obter token de acesso bruto para o ponto de extremidade do AAD Graph</span><span class="sxs-lookup"><span data-stu-id="d7229-114">Example 2 Get raw access token for AAD graph endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken -ResourceTypeName AadGraph
```

<span data-ttu-id="d7229-115">Obter o token de acesso do ponto de extremidade do AAD Graph para a conta atual</span><span class="sxs-lookup"><span data-stu-id="d7229-115">Get access token of AAD graph endpoint for current account</span></span>

### <span data-ttu-id="d7229-116">Exemplo 3 obter token de acesso bruto para o ponto de extremidade do AAD Graph</span><span class="sxs-lookup"><span data-stu-id="d7229-116">Example 3 Get raw access token for AAD graph endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken -Resource "https://graph.windows.net/"
```

<span data-ttu-id="d7229-117">Obter o token de acesso do ponto de extremidade do AAD Graph para a conta atual</span><span class="sxs-lookup"><span data-stu-id="d7229-117">Get access token of AAD graph endpoint for current account</span></span>

## <span data-ttu-id="d7229-118">OS</span><span class="sxs-lookup"><span data-stu-id="d7229-118">PARAMETERS</span></span>

### <span data-ttu-id="d7229-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7229-119">-DefaultProfile</span></span>
<span data-ttu-id="d7229-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d7229-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7229-121">-ResourceTypename</span><span class="sxs-lookup"><span data-stu-id="d7229-121">-ResourceTypeName</span></span>
<span data-ttu-id="d7229-122">Nome do tipo de recurso opcional, valores com suporte: AadGraph, AnalysisServices, ARM, atestado, Batch, datalake, keyvault, OperationalInsights, ResourceManager, Synapse.</span><span class="sxs-lookup"><span data-stu-id="d7229-122">Optional resouce type name, supported values: AadGraph, AnalysisServices, Arm, Attestation, Batch, DataLake, KeyVault, OperationalInsights, ResourceManager, Synapse.</span></span> <span data-ttu-id="d7229-123">O valor padrão é ARM se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="d7229-123">Default value is Arm if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: KnownResourceTypeName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7229-124">-ResourceUrl</span><span class="sxs-lookup"><span data-stu-id="d7229-124">-ResourceUrl</span></span>
<span data-ttu-id="d7229-125">URL do recurso para o qual você está solicitando o token, por exemplo, ' http://graph.windows.net/ '.</span><span class="sxs-lookup"><span data-stu-id="d7229-125">Resource url for that you're requesting token, e.g. 'http://graph.windows.net/'.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceUrl
Aliases: Resource, ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7229-126">-Tenantid</span><span class="sxs-lookup"><span data-stu-id="d7229-126">-TenantId</span></span>
<span data-ttu-id="d7229-127">ID de locatário opcional. Use a ID de locatário do contexto padrão, se não especificado.</span><span class="sxs-lookup"><span data-stu-id="d7229-127">Optional Tenant Id. Use tenant id of default context if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7229-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7229-128">CommonParameters</span></span>
<span data-ttu-id="d7229-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7229-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7229-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7229-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7229-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d7229-131">INPUTS</span></span>

### <span data-ttu-id="d7229-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d7229-132">None</span></span>

## <span data-ttu-id="d7229-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d7229-133">OUTPUTS</span></span>

### <span data-ttu-id="d7229-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d7229-134">System.String</span></span>

## <span data-ttu-id="d7229-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d7229-135">NOTES</span></span>

## <span data-ttu-id="d7229-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7229-136">RELATED LINKS</span></span>
