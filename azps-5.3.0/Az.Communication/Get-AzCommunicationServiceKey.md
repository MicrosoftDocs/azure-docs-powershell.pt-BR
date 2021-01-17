---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/get-azcommunicationservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationServiceKey.md
ms.openlocfilehash: e4a16b69e5919684b40d5b9f7fd4e97465d3565e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430283"
---
# <span data-ttu-id="3d719-101">Get-AzCommunicationServiceKey</span><span class="sxs-lookup"><span data-stu-id="3d719-101">Get-AzCommunicationServiceKey</span></span>

## <span data-ttu-id="3d719-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3d719-102">SYNOPSIS</span></span>
<span data-ttu-id="3d719-103">Obtenha as teclas de acesso do recurso CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="3d719-103">Get the access keys of the CommunicationService resource.</span></span>

## <span data-ttu-id="3d719-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3d719-104">SYNTAX</span></span>

```
Get-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3d719-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3d719-105">DESCRIPTION</span></span>
<span data-ttu-id="3d719-106">Obtenha as teclas de acesso do recurso CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="3d719-106">Get the access keys of the CommunicationService resource.</span></span>

## <span data-ttu-id="3d719-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3d719-107">EXAMPLES</span></span>

### <span data-ttu-id="3d719-108">Exemplo 1: buscar a chave para o serviço comunicação especificado</span><span class="sxs-lookup"><span data-stu-id="3d719-108">Example 1: Fetch the Key for the specified Communcation service</span></span>
```powershell
PS C:\> Get-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1

PrimaryConnectionString              PrimaryKey            SecondaryConnectionString               SecondaryKey
-----------------------              ----------            -----------------------                 ----------
endpoint=<example-primary-endpoint>  <example-primarykey>  endpoint=<example-secondary-endpoint>   <example-secondarykey>
```

<span data-ttu-id="3d719-109">Exibe a tecla ConnectionString e a tecla para o serviço comunicação especificado.</span><span class="sxs-lookup"><span data-stu-id="3d719-109">Displays the ConnectionString and Key for the specified Communcation service.</span></span>

## <span data-ttu-id="3d719-110">OS</span><span class="sxs-lookup"><span data-stu-id="3d719-110">PARAMETERS</span></span>

### <span data-ttu-id="3d719-111">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="3d719-111">-CommunicationServiceName</span></span>
<span data-ttu-id="3d719-112">O nome do recurso CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="3d719-112">The name of the CommunicationService resource.</span></span>

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

### <span data-ttu-id="3d719-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d719-113">-DefaultProfile</span></span>
<span data-ttu-id="3d719-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3d719-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d719-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d719-115">-ResourceGroupName</span></span>
<span data-ttu-id="3d719-116">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="3d719-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="3d719-117">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="3d719-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="3d719-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3d719-118">-SubscriptionId</span></span>
<span data-ttu-id="3d719-119">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3d719-119">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="3d719-120">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="3d719-120">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3d719-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3d719-121">-Confirm</span></span>
<span data-ttu-id="3d719-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d719-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d719-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d719-123">-WhatIf</span></span>
<span data-ttu-id="3d719-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3d719-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d719-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3d719-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d719-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d719-126">CommonParameters</span></span>
<span data-ttu-id="3d719-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d719-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d719-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d719-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d719-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3d719-129">INPUTS</span></span>

## <span data-ttu-id="3d719-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3d719-130">OUTPUTS</span></span>

### <span data-ttu-id="3d719-131">Microsoft. Azure. PowerShell. cmdlets. Communication. Models. Api20200820Preview. ICommunicationServiceKeys</span><span class="sxs-lookup"><span data-stu-id="3d719-131">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span></span>

## <span data-ttu-id="3d719-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3d719-132">NOTES</span></span>

<span data-ttu-id="3d719-133">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3d719-133">ALIASES</span></span>

## <span data-ttu-id="3d719-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3d719-134">RELATED LINKS</span></span>

