---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/get-azappconfigurationstorekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStoreKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStoreKey.md
ms.openlocfilehash: b33827640108077504b3142b58a1d8a71c8ffc95
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115552"
---
# <span data-ttu-id="bea64-101">Get-AzAppConfigurationStoreKey</span><span class="sxs-lookup"><span data-stu-id="bea64-101">Get-AzAppConfigurationStoreKey</span></span>

## <span data-ttu-id="bea64-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bea64-102">SYNOPSIS</span></span>
<span data-ttu-id="bea64-103">Lista a chave de acesso do armazenamento de configurações especificado.</span><span class="sxs-lookup"><span data-stu-id="bea64-103">Lists the access key for the specified configuration store.</span></span>

## <span data-ttu-id="bea64-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bea64-104">SYNTAX</span></span>

```
Get-AzAppConfigurationStoreKey -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bea64-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="bea64-105">DESCRIPTION</span></span>
<span data-ttu-id="bea64-106">Lista a chave de acesso do armazenamento de configurações especificado.</span><span class="sxs-lookup"><span data-stu-id="bea64-106">Lists the access key for the specified configuration store.</span></span>

## <span data-ttu-id="bea64-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bea64-107">EXAMPLES</span></span>

### <span data-ttu-id="bea64-108">Exemplo 1: Listar todas as chaves de uma loja de configuração de aplicativos</span><span class="sxs-lookup"><span data-stu-id="bea64-108">Example 1: List all store keys of an app configuration store</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test

ConnectionString                                                                                                                     LastModified        Name                ReadOnly Value
----------------                                                                                                                     ------------        ----                -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=TvV0-l0-s0:osSixtp4xggJYFlsJyYl;Secret=Bfxnosrs952PTGxvb2bdFtlTDCBPFDTlBATuEO5kRbc= 5/7/2020 9:09:27 AM Primary             False    Bfxnosrs952PTGxvb2bdFtlTDCBPFDTlBATuEO5k...
Endpoint=https://appconfig-test01.azconfig.io;Id=gcxl-l0-s0:JfSn6JA9UFkRj7/3GVTu;Secret=0fH4qQ+LLvKUKEiT3kICQTEbV0WNMi4xNu9RZxPx6X0= 5/7/2020 9:09:27 AM Secondary           False    0fH4qQ+LLvKUKEiT3kICQTEbV0WNMi4xNu9RZxPx...
Endpoint=https://appconfig-test01.azconfig.io;Id=Sl1p-l0-s0:jVozhIOYoXZ9k5pCjWa2;Secret=bAmj8BqcHguVraXNAJfuD1bDR+gzlfk2hf8ZSZhE9Ik= 5/7/2020 9:09:27 AM Primary Read Only   True     bAmj8BqcHguVraXNAJfuD1bDR+gzlfk2hf8ZSZhE...
Endpoint=https://appconfig-test01.azconfig.io;Id=htND-l0-s0:GN83PmhOFYlAlcXHN2/6;Secret=n2tp5evU2F4Z1QkctG2TgZkgMxojEkod3KTEaEgcSMQ= 5/7/2020 9:09:27 AM Secondary Read Only True     n2tp5evU2F4Z1QkctG2TgZkgMxojEkod3KTEaEgc...
```

<span data-ttu-id="bea64-109">Esse comando lista todas as chaves de armazenamento de um armazenamento de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="bea64-109">This command lists all store keys of an app configuration store.</span></span>

## <span data-ttu-id="bea64-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bea64-110">PARAMETERS</span></span>

### <span data-ttu-id="bea64-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bea64-111">-DefaultProfile</span></span>
<span data-ttu-id="bea64-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bea64-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bea64-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="bea64-113">-Name</span></span>
<span data-ttu-id="bea64-114">O nome do armazenamento de configuração.</span><span class="sxs-lookup"><span data-stu-id="bea64-114">The name of the configuration store.</span></span>

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

### <span data-ttu-id="bea64-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bea64-115">-ResourceGroupName</span></span>
<span data-ttu-id="bea64-116">O nome do grupo de recursos ao qual o registro de contêiner pertence.</span><span class="sxs-lookup"><span data-stu-id="bea64-116">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="bea64-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bea64-117">-SubscriptionId</span></span>
<span data-ttu-id="bea64-118">A ID de assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bea64-118">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="bea64-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="bea64-119">-Confirm</span></span>
<span data-ttu-id="bea64-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bea64-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bea64-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bea64-121">-WhatIf</span></span>
<span data-ttu-id="bea64-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="bea64-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bea64-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bea64-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bea64-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bea64-124">CommonParameters</span></span>
<span data-ttu-id="bea64-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bea64-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bea64-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bea64-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bea64-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="bea64-127">INPUTS</span></span>

## <span data-ttu-id="bea64-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="bea64-128">OUTPUTS</span></span>

### <span data-ttu-id="bea64-129">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span><span class="sxs-lookup"><span data-stu-id="bea64-129">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span></span>

## <span data-ttu-id="bea64-130">Notas</span><span class="sxs-lookup"><span data-stu-id="bea64-130">NOTES</span></span>

<span data-ttu-id="bea64-131">Aliases</span><span class="sxs-lookup"><span data-stu-id="bea64-131">ALIASES</span></span>

## <span data-ttu-id="bea64-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bea64-132">RELATED LINKS</span></span>

