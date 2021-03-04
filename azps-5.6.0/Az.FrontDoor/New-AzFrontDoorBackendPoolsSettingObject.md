---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolssettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
ms.openlocfilehash: c61c39bc95ae3521d7b0b573c43e303749999cbd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887772"
---
# <span data-ttu-id="d3fdc-101">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="d3fdc-101">New-AzFrontDoorBackendPoolsSettingObject</span></span>

## <span data-ttu-id="d3fdc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3fdc-102">SYNOPSIS</span></span>
<span data-ttu-id="d3fdc-103">Crie um objeto PSBackendPoolsSetting para criação do Front Door.</span><span class="sxs-lookup"><span data-stu-id="d3fdc-103">Create a PSBackendPoolsSetting object for Front Door creation.</span></span>

## <span data-ttu-id="d3fdc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d3fdc-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolsSettingObject [-EnforceCertificateNameCheck <PSEnabledState>]
 [-SendRecvTimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3fdc-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d3fdc-105">DESCRIPTION</span></span>
<span data-ttu-id="d3fdc-106">O cmdlet **New-AzFrontDoorBackendpoolsSettingObject** cria um novo objeto PSBackendPoolsSettings para criação da Porta da Frente.</span><span class="sxs-lookup"><span data-stu-id="d3fdc-106">The **New-AzFrontDoorBackendpoolsSettingObject** cmdlet creates a new PSBackendPoolsSettings object for Front Door creation.</span></span>

## <span data-ttu-id="d3fdc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d3fdc-107">EXAMPLES</span></span>

### <span data-ttu-id="d3fdc-108">Exemplo 1: Criar objeto BackendPoolsSettings usando padrões</span><span class="sxs-lookup"><span data-stu-id="d3fdc-108">Example 1: Create BackendPoolsSettings object using defaults</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 30
Id                          :
Name                        :
Type                        :
```

### <span data-ttu-id="d3fdc-109">Exemplo 2: Criar objeto BackendPoolsSettings com valores especificados pelo usuário</span><span class="sxs-lookup"><span data-stu-id="d3fdc-109">Example 2: Create BackendPoolsSettings object with user specified values</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject -SendRecvTimeoutInSeconds 60 -EnforceCertificateNameCheck Enabled


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 60
Id                          :
Name                        :
Type                        :
```

## <span data-ttu-id="d3fdc-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d3fdc-110">PARAMETERS</span></span>

### <span data-ttu-id="d3fdc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3fdc-111">-DefaultProfile</span></span>
<span data-ttu-id="d3fdc-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d3fdc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3fdc-113">-EnforceCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="d3fdc-113">-EnforceCertificateNameCheck</span></span>
<span data-ttu-id="d3fdc-114">Se deve impor a verificação de nome de certificado em solicitações HTTPS a todos os pools de back-end.</span><span class="sxs-lookup"><span data-stu-id="d3fdc-114">Whether to enforce certificate name check on HTTPS requests to all backend pools.</span></span>
<span data-ttu-id="d3fdc-115">Não há efeito em solicitações que não são HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d3fdc-115">No effect on non-HTTPS requests.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3fdc-116">-SendRecvTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="d3fdc-116">-SendRecvTimeoutInSeconds</span></span>
<span data-ttu-id="d3fdc-117">Enviar e receber tempo de espera na solicitação de encaminhamento para o back-end.</span><span class="sxs-lookup"><span data-stu-id="d3fdc-117">Send and receive timeout on forwarding request to the backend.</span></span> <span data-ttu-id="d3fdc-118">Quando o tempo final é atingido, a solicitação falha e retorna.</span><span class="sxs-lookup"><span data-stu-id="d3fdc-118">When timeout is reached, the request fails and returns.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3fdc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3fdc-119">CommonParameters</span></span>
<span data-ttu-id="d3fdc-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3fdc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3fdc-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3fdc-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3fdc-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3fdc-122">INPUTS</span></span>

### <span data-ttu-id="d3fdc-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d3fdc-123">None</span></span>

## <span data-ttu-id="d3fdc-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d3fdc-124">OUTPUTS</span></span>

### <span data-ttu-id="d3fdc-125">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="d3fdc-125">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting</span></span>

## <span data-ttu-id="d3fdc-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="d3fdc-126">NOTES</span></span>

## <span data-ttu-id="d3fdc-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3fdc-127">RELATED LINKS</span></span>
