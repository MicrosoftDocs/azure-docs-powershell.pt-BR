---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: b48222344e9a9fdb958073a658717d1cafa057f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892716"
---
# <span data-ttu-id="a4a6b-101">Get-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="a4a6b-101">Get-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="a4a6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4a6b-102">SYNOPSIS</span></span>
<span data-ttu-id="a4a6b-103">Obtém as configurações de provisionamento automático de segurança</span><span class="sxs-lookup"><span data-stu-id="a4a6b-103">Gets the security automatic provisioning settings</span></span>

## <span data-ttu-id="a4a6b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a4a6b-104">SYNTAX</span></span>

### <span data-ttu-id="a4a6b-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a4a6b-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAutoProvisioningSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4a6b-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="a4a6b-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAutoProvisioningSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a4a6b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4a6b-107">ResourceId</span></span>
```
Get-AzSecurityAutoProvisioningSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4a6b-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a4a6b-108">DESCRIPTION</span></span>
<span data-ttu-id="a4a6b-109">As Configurações de Provisionamento Automático permitem que você decida se deseja que o Centro de Segurança do Azure provisione automaticamente um agente de segurança que será instalado em suas VMs.</span><span class="sxs-lookup"><span data-stu-id="a4a6b-109">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="a4a6b-110">O agente de segurança monitorará sua VM para criar alertas de segurança e monitorar a conformidade de segurança da VM.</span><span class="sxs-lookup"><span data-stu-id="a4a6b-110">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="a4a6b-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a4a6b-111">EXAMPLES</span></span>

### <span data-ttu-id="a4a6b-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a4a6b-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="a4a6b-113">Obtém a configuração de provisionamento automático da assinatura</span><span class="sxs-lookup"><span data-stu-id="a4a6b-113">Gets the auto provisioning setting for the subscription</span></span>

## <span data-ttu-id="a4a6b-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a4a6b-114">PARAMETERS</span></span>

### <span data-ttu-id="a4a6b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4a6b-115">-DefaultProfile</span></span>
<span data-ttu-id="a4a6b-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a4a6b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4a6b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a4a6b-117">-Name</span></span>
<span data-ttu-id="a4a6b-118">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="a4a6b-118">Resource name.</span></span>

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

### <span data-ttu-id="a4a6b-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4a6b-119">-ResourceId</span></span>
<span data-ttu-id="a4a6b-120">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="a4a6b-120">Resource ID.</span></span>

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

### <span data-ttu-id="a4a6b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4a6b-121">CommonParameters</span></span>
<span data-ttu-id="a4a6b-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4a6b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4a6b-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4a6b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4a6b-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a4a6b-124">INPUTS</span></span>

### <span data-ttu-id="a4a6b-125">System.String</span><span class="sxs-lookup"><span data-stu-id="a4a6b-125">System.String</span></span>

## <span data-ttu-id="a4a6b-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a4a6b-126">OUTPUTS</span></span>

### <span data-ttu-id="a4a6b-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="a4a6b-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="a4a6b-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="a4a6b-128">NOTES</span></span>

## <span data-ttu-id="a4a6b-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a4a6b-129">RELATED LINKS</span></span>
