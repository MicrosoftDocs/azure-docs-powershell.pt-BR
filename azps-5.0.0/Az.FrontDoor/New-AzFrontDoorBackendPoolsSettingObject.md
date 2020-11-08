---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolssettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
ms.openlocfilehash: 9a5da13880b09b3527f1f515ca9ace9cb2442917
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117423"
---
# <span data-ttu-id="2277a-101">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="2277a-101">New-AzFrontDoorBackendPoolsSettingObject</span></span>

## <span data-ttu-id="2277a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2277a-102">SYNOPSIS</span></span>
<span data-ttu-id="2277a-103">Crie um objeto PSBackendPoolsSetting para a criação da porta frontal.</span><span class="sxs-lookup"><span data-stu-id="2277a-103">Create a PSBackendPoolsSetting object for Front Door creation.</span></span>

## <span data-ttu-id="2277a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2277a-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolsSettingObject [-EnforceCertificateNameCheck <PSEnabledState>]
 [-SendRecvTimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2277a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2277a-105">DESCRIPTION</span></span>
<span data-ttu-id="2277a-106">O cmdlet **New-AzFrontDoorBackendpoolsSettingObject** cria um novo objeto PSBackendPoolsSettings para a criação de porta frontal.</span><span class="sxs-lookup"><span data-stu-id="2277a-106">The **New-AzFrontDoorBackendpoolsSettingObject** cmdlet creates a new PSBackendPoolsSettings object for Front Door creation.</span></span>

## <span data-ttu-id="2277a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2277a-107">EXAMPLES</span></span>

### <span data-ttu-id="2277a-108">Exemplo 1: criar objeto BackendPoolsSettings usando padrões</span><span class="sxs-lookup"><span data-stu-id="2277a-108">Example 1: Create BackendPoolsSettings object using defaults</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 30
Id                          :
Name                        :
Type                        :
```

### <span data-ttu-id="2277a-109">Exemplo 2: criar objeto BackendPoolsSettings com valores especificados pelo usuário</span><span class="sxs-lookup"><span data-stu-id="2277a-109">Example 2: Create BackendPoolsSettings object with user specified values</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject -SendRecvTimeoutInSeconds 60 -EnforceCertificateNameCheck Enabled


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 60
Id                          :
Name                        :
Type                        :
```

## <span data-ttu-id="2277a-110">OS</span><span class="sxs-lookup"><span data-stu-id="2277a-110">PARAMETERS</span></span>

### <span data-ttu-id="2277a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2277a-111">-DefaultProfile</span></span>
<span data-ttu-id="2277a-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2277a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2277a-113">-EnforceCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="2277a-113">-EnforceCertificateNameCheck</span></span>
<span data-ttu-id="2277a-114">Se a verificação de nome do certificado deve ser aplicada em solicitações HTTPS para todos os pools back-end.</span><span class="sxs-lookup"><span data-stu-id="2277a-114">Whether to enforce certificate name check on HTTPS requests to all backend pools.</span></span>
<span data-ttu-id="2277a-115">Nenhum efeito em solicitações não HTTPS.</span><span class="sxs-lookup"><span data-stu-id="2277a-115">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="2277a-116">-SendRecvTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="2277a-116">-SendRecvTimeoutInSeconds</span></span>
<span data-ttu-id="2277a-117">Envio e recebimento do tempo limite na solicitação de encaminhamento para o back-end.</span><span class="sxs-lookup"><span data-stu-id="2277a-117">Send and receive timeout on forwarding request to the backend.</span></span> <span data-ttu-id="2277a-118">Quando o tempo limite é atingido, a solicitação falha e retorna.</span><span class="sxs-lookup"><span data-stu-id="2277a-118">When timeout is reached, the request fails and returns.</span></span>

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

### <span data-ttu-id="2277a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2277a-119">CommonParameters</span></span>
<span data-ttu-id="2277a-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2277a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2277a-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2277a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2277a-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2277a-122">INPUTS</span></span>

### <span data-ttu-id="2277a-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2277a-123">None</span></span>

## <span data-ttu-id="2277a-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2277a-124">OUTPUTS</span></span>

### <span data-ttu-id="2277a-125">Microsoft. Azure. Commands. FrontDoor. Models. PSBackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="2277a-125">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting</span></span>

## <span data-ttu-id="2277a-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2277a-126">NOTES</span></span>

## <span data-ttu-id="2277a-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2277a-127">RELATED LINKS</span></span>
