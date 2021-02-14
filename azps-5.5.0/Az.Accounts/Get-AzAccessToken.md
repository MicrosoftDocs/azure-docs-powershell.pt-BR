---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azaccesstoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
ms.openlocfilehash: 696ae59cb5115181605b7e6e647e2eb7d2792fd8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115573"
---
# <span data-ttu-id="4f1e3-101">Get-AzAccessToken</span><span class="sxs-lookup"><span data-stu-id="4f1e3-101">Get-AzAccessToken</span></span>

## <span data-ttu-id="4f1e3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4f1e3-102">SYNOPSIS</span></span>
<span data-ttu-id="4f1e3-103">Obter token de acesso bruto.</span><span class="sxs-lookup"><span data-stu-id="4f1e3-103">Get raw access token.</span></span> <span data-ttu-id="4f1e3-104">Ao usar -ResourceUrl, verifique se o valor é igual ao ambiente atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="4f1e3-104">When using -ResourceUrl, please make sure the value does match current Azure environment.</span></span> <span data-ttu-id="4f1e3-105">Você pode se referir ao valor de `(Get-AzContext).Environment` .</span><span class="sxs-lookup"><span data-stu-id="4f1e3-105">You may refer to the value of `(Get-AzContext).Environment`.</span></span>

## <span data-ttu-id="4f1e3-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4f1e3-106">SYNTAX</span></span>

### <span data-ttu-id="4f1e3-107">KnownResourceTypeName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4f1e3-107">KnownResourceTypeName (Default)</span></span>
```
Get-AzAccessToken [-ResourceTypeName <String>] [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4f1e3-108">ResourceUrl</span><span class="sxs-lookup"><span data-stu-id="4f1e3-108">ResourceUrl</span></span>
```
Get-AzAccessToken -ResourceUrl <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4f1e3-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="4f1e3-109">DESCRIPTION</span></span>
<span data-ttu-id="4f1e3-110">Obter token de acesso</span><span class="sxs-lookup"><span data-stu-id="4f1e3-110">Get access token</span></span>

## <span data-ttu-id="4f1e3-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4f1e3-111">EXAMPLES</span></span>

### <span data-ttu-id="4f1e3-112">Exemplo 1 Obter token de acesso bruto para o ponto de extremidade ARM</span><span class="sxs-lookup"><span data-stu-id="4f1e3-112">Example 1 Get raw access token for ARM endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken
```

<span data-ttu-id="4f1e3-113">Obter token de acesso do ponto de extremidade ResourceManager para a conta atual</span><span class="sxs-lookup"><span data-stu-id="4f1e3-113">Get access token of ResourceManager endpoint for current account</span></span>

### <span data-ttu-id="4f1e3-114">Exemplo 2 Obter token de acesso bruto para o ponto de extremidade do AAD Graph</span><span class="sxs-lookup"><span data-stu-id="4f1e3-114">Example 2 Get raw access token for AAD graph endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken -ResourceTypeName AadGraph
```

<span data-ttu-id="4f1e3-115">Obter token de acesso do ponto de extremidade do gráfico AAD para a conta atual</span><span class="sxs-lookup"><span data-stu-id="4f1e3-115">Get access token of AAD graph endpoint for current account</span></span>

### <span data-ttu-id="4f1e3-116">Exemplo 3 Obter token de acesso bruto para o ponto de extremidade do AAD Graph</span><span class="sxs-lookup"><span data-stu-id="4f1e3-116">Example 3 Get raw access token for AAD graph endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken -Resource "https://graph.windows.net/"
```

<span data-ttu-id="4f1e3-117">Obter token de acesso do ponto de extremidade do gráfico AAD para a conta atual</span><span class="sxs-lookup"><span data-stu-id="4f1e3-117">Get access token of AAD graph endpoint for current account</span></span>

## <span data-ttu-id="4f1e3-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4f1e3-118">PARAMETERS</span></span>

### <span data-ttu-id="4f1e3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f1e3-119">-DefaultProfile</span></span>
<span data-ttu-id="4f1e3-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4f1e3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f1e3-121">-ResourceTypeName</span><span class="sxs-lookup"><span data-stu-id="4f1e3-121">-ResourceTypeName</span></span>
<span data-ttu-id="4f1e3-122">Nome do tipo resouce opcional, valores com suporte: AadGraph, AnalysisServices, Arm, Attestation, Batch, DataLake, KeyVault, OperationalInsights, ResourceManager, Synapse.</span><span class="sxs-lookup"><span data-stu-id="4f1e3-122">Optional resouce type name, supported values: AadGraph, AnalysisServices, Arm, Attestation, Batch, DataLake, KeyVault, OperationalInsights, ResourceManager, Synapse.</span></span> <span data-ttu-id="4f1e3-123">O valor padrão é Arm, se não especificado.</span><span class="sxs-lookup"><span data-stu-id="4f1e3-123">Default value is Arm if not specified.</span></span>

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

### <span data-ttu-id="4f1e3-124">-ResourceUrl</span><span class="sxs-lookup"><span data-stu-id="4f1e3-124">-ResourceUrl</span></span>
<span data-ttu-id="4f1e3-125">URL do recurso para o que você está solicitando token, por exemplo' http://graph.windows.net/ '.</span><span class="sxs-lookup"><span data-stu-id="4f1e3-125">Resource url for that you're requesting token, e.g. 'http://graph.windows.net/'.</span></span>

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

### <span data-ttu-id="4f1e3-126">-TenantId</span><span class="sxs-lookup"><span data-stu-id="4f1e3-126">-TenantId</span></span>
<span data-ttu-id="4f1e3-127">ID do Locatário Opcional. Use a ID do locatário do contexto padrão, se não especificada.</span><span class="sxs-lookup"><span data-stu-id="4f1e3-127">Optional Tenant Id. Use tenant id of default context if not specified.</span></span>

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

### <span data-ttu-id="4f1e3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f1e3-128">CommonParameters</span></span>
<span data-ttu-id="4f1e3-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f1e3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f1e3-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4f1e3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f1e3-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="4f1e3-131">INPUTS</span></span>

### <span data-ttu-id="4f1e3-132">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4f1e3-132">None</span></span>

## <span data-ttu-id="4f1e3-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="4f1e3-133">OUTPUTS</span></span>

### <span data-ttu-id="4f1e3-134">System.String</span><span class="sxs-lookup"><span data-stu-id="4f1e3-134">System.String</span></span>

## <span data-ttu-id="4f1e3-135">Notas</span><span class="sxs-lookup"><span data-stu-id="4f1e3-135">NOTES</span></span>

## <span data-ttu-id="4f1e3-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4f1e3-136">RELATED LINKS</span></span>
