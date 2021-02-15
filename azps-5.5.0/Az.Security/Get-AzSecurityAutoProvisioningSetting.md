---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: 08631f5705a3a0255c42ac3d146cef45de1b4e56
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116200"
---
# <span data-ttu-id="d048e-101">Get-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="d048e-101">Get-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="d048e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d048e-102">SYNOPSIS</span></span>
<span data-ttu-id="d048e-103">Obtém as configurações de provisionamento automático de segurança</span><span class="sxs-lookup"><span data-stu-id="d048e-103">Gets the security automatic provisioning settings</span></span>

## <span data-ttu-id="d048e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d048e-104">SYNTAX</span></span>

### <span data-ttu-id="d048e-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d048e-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAutoProvisioningSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d048e-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="d048e-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAutoProvisioningSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d048e-107">Resourceid</span><span class="sxs-lookup"><span data-stu-id="d048e-107">ResourceId</span></span>
```
Get-AzSecurityAutoProvisioningSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d048e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="d048e-108">DESCRIPTION</span></span>
<span data-ttu-id="d048e-109">As Configurações de Provisionamento Automático permitem que você decida se deseja que a Central de Segurança do Azure provisione automaticamente um agente de segurança que será instalado em seus VMs.</span><span class="sxs-lookup"><span data-stu-id="d048e-109">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="d048e-110">O agente de segurança monitorará seu VM para criar alertas de segurança e monitorar a conformidade de segurança do VM.</span><span class="sxs-lookup"><span data-stu-id="d048e-110">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="d048e-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d048e-111">EXAMPLES</span></span>

### <span data-ttu-id="d048e-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d048e-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="d048e-113">Obtém a configuração de provisionamento automático para a assinatura</span><span class="sxs-lookup"><span data-stu-id="d048e-113">Gets the auto provisioning setting for the subscription</span></span>

## <span data-ttu-id="d048e-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d048e-114">PARAMETERS</span></span>

### <span data-ttu-id="d048e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d048e-115">-DefaultProfile</span></span>
<span data-ttu-id="d048e-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d048e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d048e-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="d048e-117">-Name</span></span>
<span data-ttu-id="d048e-118">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="d048e-118">Resource name.</span></span>

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

### <span data-ttu-id="d048e-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d048e-119">-ResourceId</span></span>
<span data-ttu-id="d048e-120">ID do Recurso.</span><span class="sxs-lookup"><span data-stu-id="d048e-120">Resource ID.</span></span>

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

### <span data-ttu-id="d048e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d048e-121">CommonParameters</span></span>
<span data-ttu-id="d048e-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d048e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d048e-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d048e-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d048e-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="d048e-124">INPUTS</span></span>

### <span data-ttu-id="d048e-125">System.String</span><span class="sxs-lookup"><span data-stu-id="d048e-125">System.String</span></span>

## <span data-ttu-id="d048e-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="d048e-126">OUTPUTS</span></span>

### <span data-ttu-id="d048e-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="d048e-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="d048e-128">Notas</span><span class="sxs-lookup"><span data-stu-id="d048e-128">NOTES</span></span>

## <span data-ttu-id="d048e-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d048e-129">RELATED LINKS</span></span>
