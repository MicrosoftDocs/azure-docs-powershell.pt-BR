---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/powershell/module/az.communication/get-azcommunicationservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationServiceKey.md
ms.openlocfilehash: 82e5f6ced22b17c8966afbd5bc57324ab2069d1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890472"
---
# <span data-ttu-id="3dc20-101">Get-AzCommunicationServiceKey</span><span class="sxs-lookup"><span data-stu-id="3dc20-101">Get-AzCommunicationServiceKey</span></span>

## <span data-ttu-id="3dc20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3dc20-102">SYNOPSIS</span></span>
<span data-ttu-id="3dc20-103">Obter as chaves de acesso do recurso CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="3dc20-103">Get the access keys of the CommunicationService resource.</span></span>

## <span data-ttu-id="3dc20-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3dc20-104">SYNTAX</span></span>

```
Get-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3dc20-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3dc20-105">DESCRIPTION</span></span>
<span data-ttu-id="3dc20-106">Obter as chaves de acesso do recurso CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="3dc20-106">Get the access keys of the CommunicationService resource.</span></span>

## <span data-ttu-id="3dc20-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3dc20-107">EXAMPLES</span></span>

### <span data-ttu-id="3dc20-108">Exemplo 1: Buscar a chave para o serviço de Comunicação especificado</span><span class="sxs-lookup"><span data-stu-id="3dc20-108">Example 1: Fetch the Key for the specified Communcation service</span></span>
```powershell
PS C:\> Get-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1

PrimaryConnectionString              PrimaryKey            SecondaryConnectionString               SecondaryKey
-----------------------              ----------            -----------------------                 ----------
endpoint=<example-primary-endpoint>  <example-primarykey>  endpoint=<example-secondary-endpoint>   <example-secondarykey>
```

<span data-ttu-id="3dc20-109">Exibe ConnectionString e Key para o serviço de Comunicação especificado.</span><span class="sxs-lookup"><span data-stu-id="3dc20-109">Displays the ConnectionString and Key for the specified Communcation service.</span></span>

## <span data-ttu-id="3dc20-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3dc20-110">PARAMETERS</span></span>

### <span data-ttu-id="3dc20-111">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="3dc20-111">-CommunicationServiceName</span></span>
<span data-ttu-id="3dc20-112">O nome do recurso CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="3dc20-112">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dc20-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dc20-113">-DefaultProfile</span></span>
<span data-ttu-id="3dc20-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3dc20-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dc20-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dc20-115">-ResourceGroupName</span></span>
<span data-ttu-id="3dc20-116">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="3dc20-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="3dc20-117">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="3dc20-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dc20-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3dc20-118">-SubscriptionId</span></span>
<span data-ttu-id="3dc20-119">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3dc20-119">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="3dc20-120">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="3dc20-120">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dc20-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3dc20-121">-Confirm</span></span>
<span data-ttu-id="3dc20-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3dc20-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dc20-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dc20-123">-WhatIf</span></span>
<span data-ttu-id="3dc20-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3dc20-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dc20-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3dc20-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dc20-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dc20-126">CommonParameters</span></span>
<span data-ttu-id="3dc20-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dc20-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dc20-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3dc20-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dc20-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3dc20-129">INPUTS</span></span>

## <span data-ttu-id="3dc20-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3dc20-130">OUTPUTS</span></span>

### <span data-ttu-id="3dc20-131">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span><span class="sxs-lookup"><span data-stu-id="3dc20-131">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span></span>

## <span data-ttu-id="3dc20-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="3dc20-132">NOTES</span></span>

<span data-ttu-id="3dc20-133">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3dc20-133">ALIASES</span></span>

## <span data-ttu-id="3dc20-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3dc20-134">RELATED LINKS</span></span>

