---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: 6c926b606cc764abcf3627c725596deffda395b5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944189"
---
# <span data-ttu-id="84460-101">Get-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="84460-101">Get-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="84460-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="84460-102">SYNOPSIS</span></span>
<span data-ttu-id="84460-103">Obtém as configurações de provisionamento automático de segurança</span><span class="sxs-lookup"><span data-stu-id="84460-103">Gets the security automatic provisioning settings</span></span>

## <span data-ttu-id="84460-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="84460-104">SYNTAX</span></span>

### <span data-ttu-id="84460-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="84460-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAutoProvisioningSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84460-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="84460-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAutoProvisioningSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84460-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="84460-107">ResourceId</span></span>
```
Get-AzSecurityAutoProvisioningSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="84460-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="84460-108">DESCRIPTION</span></span>
<span data-ttu-id="84460-109">As configurações de provisionamento automático permitem que você decida se deseja que a central de segurança do Azure forneça automaticamente um agente de segurança que será instalado em suas VMs.</span><span class="sxs-lookup"><span data-stu-id="84460-109">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="84460-110">O agente de segurança monitorará sua VM para criar alertas de segurança e monitorará a conformidade de segurança da VM.</span><span class="sxs-lookup"><span data-stu-id="84460-110">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="84460-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="84460-111">EXAMPLES</span></span>

### <span data-ttu-id="84460-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="84460-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="84460-113">Obtém a configuração de provisionamento automático para a assinatura</span><span class="sxs-lookup"><span data-stu-id="84460-113">Gets the auto provisioning setting for the subscription</span></span>

## <span data-ttu-id="84460-114">OS</span><span class="sxs-lookup"><span data-stu-id="84460-114">PARAMETERS</span></span>

### <span data-ttu-id="84460-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84460-115">-DefaultProfile</span></span>
<span data-ttu-id="84460-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="84460-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84460-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="84460-117">-Name</span></span>
<span data-ttu-id="84460-118">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="84460-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84460-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84460-119">-ResourceId</span></span>
<span data-ttu-id="84460-120">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="84460-120">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84460-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84460-121">CommonParameters</span></span>
<span data-ttu-id="84460-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84460-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84460-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84460-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84460-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="84460-124">INPUTS</span></span>

### <span data-ttu-id="84460-125">System. String</span><span class="sxs-lookup"><span data-stu-id="84460-125">System.String</span></span>

## <span data-ttu-id="84460-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="84460-126">OUTPUTS</span></span>

### <span data-ttu-id="84460-127">Microsoft. Azure. Commands. Security. Models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="84460-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="84460-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="84460-128">NOTES</span></span>

## <span data-ttu-id="84460-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="84460-129">RELATED LINKS</span></span>
