---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/powershell/module/az.appconfiguration/test-azappconfigurationstorenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
ms.openlocfilehash: 87d19475896138ee51a31694f707c1839f839ba8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886800"
---
# <span data-ttu-id="752b4-101">Test-AzAppConfigurationStoreNameAvailability</span><span class="sxs-lookup"><span data-stu-id="752b4-101">Test-AzAppConfigurationStoreNameAvailability</span></span>

## <span data-ttu-id="752b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="752b4-102">SYNOPSIS</span></span>
<span data-ttu-id="752b4-103">Verifica se o nome do armazenamento de configuração está disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="752b4-103">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="752b4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="752b4-104">SYNTAX</span></span>

```
Test-AzAppConfigurationStoreNameAvailability -Name <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="752b4-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="752b4-105">DESCRIPTION</span></span>
<span data-ttu-id="752b4-106">Verifica se o nome do armazenamento de configuração está disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="752b4-106">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="752b4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="752b4-107">EXAMPLES</span></span>

### <span data-ttu-id="752b4-108">Exemplo 1: Testar a disponibilidade do nome do armazenamento de configuração do aplicativo</span><span class="sxs-lookup"><span data-stu-id="752b4-108">Example 1: Test availability of the app configuration store name</span></span>

```powershell
PS C:\> Test-AzAppConfigurationStoreNameAvailability -Name appconfig-test01

Message                               NameAvailable Reason
-------                               ------------- ------
The specified name is already in use. False         AlreadyExists
```

<span data-ttu-id="752b4-109">Este comando testa a disponibilidade do nome do armazenamento de configuração do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="752b4-109">This command tests availability of the app configuration store name.</span></span>

## <span data-ttu-id="752b4-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="752b4-110">PARAMETERS</span></span>

### <span data-ttu-id="752b4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="752b4-111">-DefaultProfile</span></span>
<span data-ttu-id="752b4-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="752b4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="752b4-113">-Name</span><span class="sxs-lookup"><span data-stu-id="752b4-113">-Name</span></span>
<span data-ttu-id="752b4-114">O nome para verificar a disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="752b4-114">The name to check for availability.</span></span>

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

### <span data-ttu-id="752b4-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="752b4-115">-SubscriptionId</span></span>
<span data-ttu-id="752b4-116">A ID de assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="752b4-116">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="752b4-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="752b4-117">-Confirm</span></span>
<span data-ttu-id="752b4-118">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="752b4-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="752b4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="752b4-119">-WhatIf</span></span>
<span data-ttu-id="752b4-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="752b4-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="752b4-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="752b4-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="752b4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="752b4-122">CommonParameters</span></span>
<span data-ttu-id="752b4-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="752b4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="752b4-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="752b4-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="752b4-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="752b4-125">INPUTS</span></span>

## <span data-ttu-id="752b4-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="752b4-126">OUTPUTS</span></span>

### <span data-ttu-id="752b4-127">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.INameAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="752b4-127">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.INameAvailabilityStatus</span></span>

## <span data-ttu-id="752b4-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="752b4-128">NOTES</span></span>

<span data-ttu-id="752b4-129">ALIASES</span><span class="sxs-lookup"><span data-stu-id="752b4-129">ALIASES</span></span>

## <span data-ttu-id="752b4-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="752b4-130">RELATED LINKS</span></span>

