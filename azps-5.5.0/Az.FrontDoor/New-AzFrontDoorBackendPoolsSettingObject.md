---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolssettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
ms.openlocfilehash: 9a5da13880b09b3527f1f515ca9ace9cb2442917
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116802"
---
# <span data-ttu-id="097c8-101">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="097c8-101">New-AzFrontDoorBackendPoolsSettingObject</span></span>

## <span data-ttu-id="097c8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="097c8-102">SYNOPSIS</span></span>
<span data-ttu-id="097c8-103">Crie um objeto PSBackendPoolsSetting para criação de Porta Da Frente.</span><span class="sxs-lookup"><span data-stu-id="097c8-103">Create a PSBackendPoolsSetting object for Front Door creation.</span></span>

## <span data-ttu-id="097c8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="097c8-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolsSettingObject [-EnforceCertificateNameCheck <PSEnabledState>]
 [-SendRecvTimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="097c8-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="097c8-105">DESCRIPTION</span></span>
<span data-ttu-id="097c8-106">O cmdlet **New-AzFrontDoorBackendpoolsSettingObject** cria um novo objeto PSBackendPoolsSettings para criação da Porta da Frente.</span><span class="sxs-lookup"><span data-stu-id="097c8-106">The **New-AzFrontDoorBackendpoolsSettingObject** cmdlet creates a new PSBackendPoolsSettings object for Front Door creation.</span></span>

## <span data-ttu-id="097c8-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="097c8-107">EXAMPLES</span></span>

### <span data-ttu-id="097c8-108">Exemplo 1: Criar objeto BackendPoolsSettings usando padrões</span><span class="sxs-lookup"><span data-stu-id="097c8-108">Example 1: Create BackendPoolsSettings object using defaults</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 30
Id                          :
Name                        :
Type                        :
```

### <span data-ttu-id="097c8-109">Exemplo 2: Criar objeto BackendPoolsSettings com valores especificados pelo usuário</span><span class="sxs-lookup"><span data-stu-id="097c8-109">Example 2: Create BackendPoolsSettings object with user specified values</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject -SendRecvTimeoutInSeconds 60 -EnforceCertificateNameCheck Enabled


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 60
Id                          :
Name                        :
Type                        :
```

## <span data-ttu-id="097c8-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="097c8-110">PARAMETERS</span></span>

### <span data-ttu-id="097c8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="097c8-111">-DefaultProfile</span></span>
<span data-ttu-id="097c8-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="097c8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="097c8-113">-EnforceCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="097c8-113">-EnforceCertificateNameCheck</span></span>
<span data-ttu-id="097c8-114">Se você quer impor a verificação de nome de certificado em solicitações HTTPS a todos os pools de back-end.</span><span class="sxs-lookup"><span data-stu-id="097c8-114">Whether to enforce certificate name check on HTTPS requests to all backend pools.</span></span>
<span data-ttu-id="097c8-115">Não há efeito em solicitações que não são HTTPS.</span><span class="sxs-lookup"><span data-stu-id="097c8-115">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="097c8-116">-SendRecvTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="097c8-116">-SendRecvTimeoutInSeconds</span></span>
<span data-ttu-id="097c8-117">Enviar e receber tempo de tempo de espera sobre a solicitação de encaminhamento para o back-end.</span><span class="sxs-lookup"><span data-stu-id="097c8-117">Send and receive timeout on forwarding request to the backend.</span></span> <span data-ttu-id="097c8-118">Quando o tempo é atingido, a solicitação falha e retorna.</span><span class="sxs-lookup"><span data-stu-id="097c8-118">When timeout is reached, the request fails and returns.</span></span>

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

### <span data-ttu-id="097c8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="097c8-119">CommonParameters</span></span>
<span data-ttu-id="097c8-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="097c8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="097c8-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="097c8-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="097c8-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="097c8-122">INPUTS</span></span>

### <span data-ttu-id="097c8-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="097c8-123">None</span></span>

## <span data-ttu-id="097c8-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="097c8-124">OUTPUTS</span></span>

### <span data-ttu-id="097c8-125">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="097c8-125">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting</span></span>

## <span data-ttu-id="097c8-126">Notas</span><span class="sxs-lookup"><span data-stu-id="097c8-126">NOTES</span></span>

## <span data-ttu-id="097c8-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="097c8-127">RELATED LINKS</span></span>
