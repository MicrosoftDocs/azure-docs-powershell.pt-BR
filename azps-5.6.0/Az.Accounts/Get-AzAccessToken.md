---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-azaccesstoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
ms.openlocfilehash: 5fcd81dcfc69f020a4e17e0858abfca0edaba405
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888014"
---
# <span data-ttu-id="dbc61-101">Get-AzAccessToken</span><span class="sxs-lookup"><span data-stu-id="dbc61-101">Get-AzAccessToken</span></span>

## <span data-ttu-id="dbc61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbc61-102">SYNOPSIS</span></span>
<span data-ttu-id="dbc61-103">Obter token de acesso bruto.</span><span class="sxs-lookup"><span data-stu-id="dbc61-103">Get raw access token.</span></span> <span data-ttu-id="dbc61-104">Ao usar -ResourceUrl, verifique se o valor corresponderá ao ambiente atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="dbc61-104">When using -ResourceUrl, please make sure the value does match current Azure environment.</span></span> <span data-ttu-id="dbc61-105">Você pode se referir ao valor de `(Get-AzContext).Environment` .</span><span class="sxs-lookup"><span data-stu-id="dbc61-105">You may refer to the value of `(Get-AzContext).Environment`.</span></span>

## <span data-ttu-id="dbc61-106">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="dbc61-106">SYNTAX</span></span>

### <span data-ttu-id="dbc61-107">KnownResourceTypeName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="dbc61-107">KnownResourceTypeName (Default)</span></span>
```
Get-AzAccessToken [-ResourceTypeName <String>] [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dbc61-108">ResourceUrl</span><span class="sxs-lookup"><span data-stu-id="dbc61-108">ResourceUrl</span></span>
```
Get-AzAccessToken -ResourceUrl <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dbc61-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dbc61-109">DESCRIPTION</span></span>
<span data-ttu-id="dbc61-110">Obter token de acesso</span><span class="sxs-lookup"><span data-stu-id="dbc61-110">Get access token</span></span>

## <span data-ttu-id="dbc61-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dbc61-111">EXAMPLES</span></span>

### <span data-ttu-id="dbc61-112">Exemplo 1 Obter token de acesso bruto para ARM ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="dbc61-112">Example 1 Get raw access token for ARM endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken
```

<span data-ttu-id="dbc61-113">Obter token de acesso do ponto de extremidade ResourceManager para conta atual</span><span class="sxs-lookup"><span data-stu-id="dbc61-113">Get access token of ResourceManager endpoint for current account</span></span>

### <span data-ttu-id="dbc61-114">Exemplo 2 Obter token de acesso bruto para ponto de extremidade do gráfico AAD</span><span class="sxs-lookup"><span data-stu-id="dbc61-114">Example 2 Get raw access token for AAD graph endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken -ResourceTypeName AadGraph
```

<span data-ttu-id="dbc61-115">Obter token de acesso do ponto de extremidade do gráfico AAD para conta atual</span><span class="sxs-lookup"><span data-stu-id="dbc61-115">Get access token of AAD graph endpoint for current account</span></span>

### <span data-ttu-id="dbc61-116">Exemplo 3 Obter token de acesso bruto para ponto de extremidade do gráfico AAD</span><span class="sxs-lookup"><span data-stu-id="dbc61-116">Example 3 Get raw access token for AAD graph endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken -Resource "https://graph.windows.net/"
```

<span data-ttu-id="dbc61-117">Obter token de acesso do ponto de extremidade do gráfico AAD para conta atual</span><span class="sxs-lookup"><span data-stu-id="dbc61-117">Get access token of AAD graph endpoint for current account</span></span>

## <span data-ttu-id="dbc61-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="dbc61-118">PARAMETERS</span></span>

### <span data-ttu-id="dbc61-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbc61-119">-DefaultProfile</span></span>
<span data-ttu-id="dbc61-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dbc61-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbc61-121">-ResourceTypeName</span><span class="sxs-lookup"><span data-stu-id="dbc61-121">-ResourceTypeName</span></span>
<span data-ttu-id="dbc61-122">Nome do tipo resouce opcional, valores com suporte: AadGraph, AnalysisServices, Arm, Attestation, Batch, DataLake, KeyVault, OperationalInsights, ResourceManager, Synapse.</span><span class="sxs-lookup"><span data-stu-id="dbc61-122">Optional resouce type name, supported values: AadGraph, AnalysisServices, Arm, Attestation, Batch, DataLake, KeyVault, OperationalInsights, ResourceManager, Synapse.</span></span> <span data-ttu-id="dbc61-123">O valor padrão é Arm, se não especificado.</span><span class="sxs-lookup"><span data-stu-id="dbc61-123">Default value is Arm if not specified.</span></span>

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

### <span data-ttu-id="dbc61-124">-ResourceUrl</span><span class="sxs-lookup"><span data-stu-id="dbc61-124">-ResourceUrl</span></span>
<span data-ttu-id="dbc61-125">Url de recurso para o que você está solicitando token, por exemplo' http://graph.windows.net/ '.</span><span class="sxs-lookup"><span data-stu-id="dbc61-125">Resource url for that you're requesting token, e.g. 'http://graph.windows.net/'.</span></span>

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

### <span data-ttu-id="dbc61-126">-TenantId</span><span class="sxs-lookup"><span data-stu-id="dbc61-126">-TenantId</span></span>
<span data-ttu-id="dbc61-127">ID de locatário opcional. Use id de locatário do contexto padrão, se não especificado.</span><span class="sxs-lookup"><span data-stu-id="dbc61-127">Optional Tenant Id. Use tenant id of default context if not specified.</span></span>

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

### <span data-ttu-id="dbc61-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbc61-128">CommonParameters</span></span>
<span data-ttu-id="dbc61-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbc61-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbc61-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dbc61-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbc61-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dbc61-131">INPUTS</span></span>

### <span data-ttu-id="dbc61-132">Nenhum</span><span class="sxs-lookup"><span data-stu-id="dbc61-132">None</span></span>

## <span data-ttu-id="dbc61-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="dbc61-133">OUTPUTS</span></span>

### <span data-ttu-id="dbc61-134">System.String</span><span class="sxs-lookup"><span data-stu-id="dbc61-134">System.String</span></span>

## <span data-ttu-id="dbc61-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="dbc61-135">NOTES</span></span>

## <span data-ttu-id="dbc61-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dbc61-136">RELATED LINKS</span></span>
