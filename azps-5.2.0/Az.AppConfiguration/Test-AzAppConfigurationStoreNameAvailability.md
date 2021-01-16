---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/test-azappconfigurationstorenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
ms.openlocfilehash: c7f315d1989a6cbbfbfa08cf3f59cff8ccd811bc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98256714"
---
# <span data-ttu-id="daf9a-101">Test-AzAppConfigurationStoreNameAvailability</span><span class="sxs-lookup"><span data-stu-id="daf9a-101">Test-AzAppConfigurationStoreNameAvailability</span></span>

## <span data-ttu-id="daf9a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="daf9a-102">SYNOPSIS</span></span>
<span data-ttu-id="daf9a-103">Verifica se o nome do repositório de configuração está disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="daf9a-103">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="daf9a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="daf9a-104">SYNTAX</span></span>

```
Test-AzAppConfigurationStoreNameAvailability -Name <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="daf9a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="daf9a-105">DESCRIPTION</span></span>
<span data-ttu-id="daf9a-106">Verifica se o nome do repositório de configuração está disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="daf9a-106">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="daf9a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="daf9a-107">EXAMPLES</span></span>

### <span data-ttu-id="daf9a-108">Exemplo 1: testar a disponibilidade do nome do repositório de configuração do aplicativo</span><span class="sxs-lookup"><span data-stu-id="daf9a-108">Example 1: Test availability of the app configuration store name</span></span>

```powershell
PS C:\> Test-AzAppConfigurationStoreNameAvailability -Name appconfig-test01

Message                               NameAvailable Reason
-------                               ------------- ------
The specified name is already in use. False         AlreadyExists
```

<span data-ttu-id="daf9a-109">Esse comando testa a disponibilidade do nome da loja de configuração do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="daf9a-109">This command tests availability of the app configuration store name.</span></span>

## <span data-ttu-id="daf9a-110">OS</span><span class="sxs-lookup"><span data-stu-id="daf9a-110">PARAMETERS</span></span>

### <span data-ttu-id="daf9a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daf9a-111">-DefaultProfile</span></span>
<span data-ttu-id="daf9a-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="daf9a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="daf9a-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="daf9a-113">-Name</span></span>
<span data-ttu-id="daf9a-114">O nome para verificar a disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="daf9a-114">The name to check for availability.</span></span>

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

### <span data-ttu-id="daf9a-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="daf9a-115">-SubscriptionId</span></span>
<span data-ttu-id="daf9a-116">A ID da assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="daf9a-116">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="daf9a-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="daf9a-117">-Confirm</span></span>
<span data-ttu-id="daf9a-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="daf9a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="daf9a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="daf9a-119">-WhatIf</span></span>
<span data-ttu-id="daf9a-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="daf9a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="daf9a-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="daf9a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="daf9a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daf9a-122">CommonParameters</span></span>
<span data-ttu-id="daf9a-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="daf9a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daf9a-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="daf9a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daf9a-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="daf9a-125">INPUTS</span></span>

## <span data-ttu-id="daf9a-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="daf9a-126">OUTPUTS</span></span>

### <span data-ttu-id="daf9a-127">Microsoft. Azure. PowerShell. cmdlets. AppConfiguration. Models. Api20200601. INameAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="daf9a-127">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.INameAvailabilityStatus</span></span>

## <span data-ttu-id="daf9a-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="daf9a-128">NOTES</span></span>

<span data-ttu-id="daf9a-129">ALIASES</span><span class="sxs-lookup"><span data-stu-id="daf9a-129">ALIASES</span></span>

## <span data-ttu-id="daf9a-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="daf9a-130">RELATED LINKS</span></span>

