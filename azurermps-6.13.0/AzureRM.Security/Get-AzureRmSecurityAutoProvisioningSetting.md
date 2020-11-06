---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityAutoProvisioningSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityAutoProvisioningSetting.md
ms.openlocfilehash: 98adc5714f4a4abaeca9fe6723b1a56fe1d49fca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609746"
---
# <span data-ttu-id="52071-101">Get-AzureRmSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="52071-101">Get-AzureRmSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="52071-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52071-102">SYNOPSIS</span></span>
<span data-ttu-id="52071-103">Obtém as configurações de provisionamento automático de segurança</span><span class="sxs-lookup"><span data-stu-id="52071-103">Gets the security automatic provisioning settings</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52071-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52071-104">SYNTAX</span></span>

### <span data-ttu-id="52071-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="52071-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityAutoProvisioningSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52071-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="52071-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityAutoProvisioningSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="52071-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="52071-107">ResourceId</span></span>
```
Get-AzureRmSecurityAutoProvisioningSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="52071-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52071-108">DESCRIPTION</span></span>
<span data-ttu-id="52071-109">As configurações de provisionamento automático permitem que você decida se deseja que o Cetner de segurança do Azure proviosion automaticamente um agente de segurança que será instalado em suas VMs.</span><span class="sxs-lookup"><span data-stu-id="52071-109">Automatic Provisioning Settings let you decide whether you want Azure Security Cetner to automatically proviosion a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="52071-110">O agente de segurança monitorará sua VM para criar alertas de segurança e monitorará a conformidade de segurança da VM.</span><span class="sxs-lookup"><span data-stu-id="52071-110">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="52071-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52071-111">EXAMPLES</span></span>

### <span data-ttu-id="52071-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="52071-112">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="52071-113">Obtém a configuração de provisionamento automático para a assinatura</span><span class="sxs-lookup"><span data-stu-id="52071-113">Gets the auto provisioning setting for the subscription</span></span>

## <span data-ttu-id="52071-114">OS</span><span class="sxs-lookup"><span data-stu-id="52071-114">PARAMETERS</span></span>

### <span data-ttu-id="52071-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52071-115">-DefaultProfile</span></span>
<span data-ttu-id="52071-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52071-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52071-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="52071-117">-Name</span></span>
<span data-ttu-id="52071-118">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="52071-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52071-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52071-119">-ResourceId</span></span>
<span data-ttu-id="52071-120">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="52071-120">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52071-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52071-121">CommonParameters</span></span>
<span data-ttu-id="52071-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52071-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52071-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52071-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52071-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52071-124">INPUTS</span></span>

### <span data-ttu-id="52071-125">System. String</span><span class="sxs-lookup"><span data-stu-id="52071-125">System.String</span></span>

## <span data-ttu-id="52071-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52071-126">OUTPUTS</span></span>

### <span data-ttu-id="52071-127">Microsoft. Azure. Commands. Security. Models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="52071-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="52071-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52071-128">NOTES</span></span>

## <span data-ttu-id="52071-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52071-129">RELATED LINKS</span></span>
