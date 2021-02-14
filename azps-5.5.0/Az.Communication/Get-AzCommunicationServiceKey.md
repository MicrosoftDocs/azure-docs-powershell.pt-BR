---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/get-azcommunicationservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationServiceKey.md
ms.openlocfilehash: e4a16b69e5919684b40d5b9f7fd4e97465d3565e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116564"
---
# <span data-ttu-id="9a4d6-101">Get-AzCommunicationServiceKey</span><span class="sxs-lookup"><span data-stu-id="9a4d6-101">Get-AzCommunicationServiceKey</span></span>

## <span data-ttu-id="9a4d6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9a4d6-102">SYNOPSIS</span></span>
<span data-ttu-id="9a4d6-103">Obter as chaves de acesso do recurso CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="9a4d6-103">Get the access keys of the CommunicationService resource.</span></span>

## <span data-ttu-id="9a4d6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9a4d6-104">SYNTAX</span></span>

```
Get-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9a4d6-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="9a4d6-105">DESCRIPTION</span></span>
<span data-ttu-id="9a4d6-106">Obter as chaves de acesso do recurso CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="9a4d6-106">Get the access keys of the CommunicationService resource.</span></span>

## <span data-ttu-id="9a4d6-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9a4d6-107">EXAMPLES</span></span>

### <span data-ttu-id="9a4d6-108">Exemplo 1: buscar a chave para o serviço de comunicação especificado</span><span class="sxs-lookup"><span data-stu-id="9a4d6-108">Example 1: Fetch the Key for the specified Communcation service</span></span>
```powershell
PS C:\> Get-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1

PrimaryConnectionString              PrimaryKey            SecondaryConnectionString               SecondaryKey
-----------------------              ----------            -----------------------                 ----------
endpoint=<example-primary-endpoint>  <example-primarykey>  endpoint=<example-secondary-endpoint>   <example-secondarykey>
```

<span data-ttu-id="9a4d6-109">Exibe o ConnectionString e a Tecla para o serviço de Comunicação especificado.</span><span class="sxs-lookup"><span data-stu-id="9a4d6-109">Displays the ConnectionString and Key for the specified Communcation service.</span></span>

## <span data-ttu-id="9a4d6-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9a4d6-110">PARAMETERS</span></span>

### <span data-ttu-id="9a4d6-111">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="9a4d6-111">-CommunicationServiceName</span></span>
<span data-ttu-id="9a4d6-112">O nome do recurso CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="9a4d6-112">The name of the CommunicationService resource.</span></span>

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

### <span data-ttu-id="9a4d6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a4d6-113">-DefaultProfile</span></span>
<span data-ttu-id="9a4d6-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9a4d6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a4d6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a4d6-115">-ResourceGroupName</span></span>
<span data-ttu-id="9a4d6-116">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="9a4d6-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="9a4d6-117">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="9a4d6-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="9a4d6-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9a4d6-118">-SubscriptionId</span></span>
<span data-ttu-id="9a4d6-119">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9a4d6-119">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="9a4d6-120">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="9a4d6-120">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9a4d6-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="9a4d6-121">-Confirm</span></span>
<span data-ttu-id="9a4d6-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a4d6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a4d6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a4d6-123">-WhatIf</span></span>
<span data-ttu-id="9a4d6-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="9a4d6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a4d6-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9a4d6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a4d6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a4d6-126">CommonParameters</span></span>
<span data-ttu-id="9a4d6-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a4d6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a4d6-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9a4d6-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a4d6-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="9a4d6-129">INPUTS</span></span>

## <span data-ttu-id="9a4d6-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="9a4d6-130">OUTPUTS</span></span>

### <span data-ttu-id="9a4d6-131">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span><span class="sxs-lookup"><span data-stu-id="9a4d6-131">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span></span>

## <span data-ttu-id="9a4d6-132">Notas</span><span class="sxs-lookup"><span data-stu-id="9a4d6-132">NOTES</span></span>

<span data-ttu-id="9a4d6-133">Aliases</span><span class="sxs-lookup"><span data-stu-id="9a4d6-133">ALIASES</span></span>

## <span data-ttu-id="9a4d6-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9a4d6-134">RELATED LINKS</span></span>

