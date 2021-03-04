---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 4813EE2B-16C4-4716-B6DD-9447A0B46F3D
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccountcallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCallbackUrl.md
ms.openlocfilehash: c23e8ca566db3a3b3c93dcdc7a4fc53fc85979c7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886464"
---
# <span data-ttu-id="42d41-101">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="42d41-101">Get-AzIntegrationAccountCallbackUrl</span></span>

## <span data-ttu-id="42d41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42d41-102">SYNOPSIS</span></span>
<span data-ttu-id="42d41-103">Obtém uma URL de retorno de chamada de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="42d41-103">Gets an integration account callback URL.</span></span>

## <span data-ttu-id="42d41-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="42d41-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountCallbackUrl -ResourceGroupName <String> -Name <String> [-NotAfter <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42d41-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="42d41-105">DESCRIPTION</span></span>
<span data-ttu-id="42d41-106">O cmdlet **Get-AzIntegrationAccountCallbackUrl** obtém uma URL de retorno de chamada de conta de integração de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="42d41-106">The **Get-AzIntegrationAccountCallbackUrl** cmdlet gets an integration account callback URL from a resource group.</span></span>
<span data-ttu-id="42d41-107">Este cmdlet retorna um **objeto CallbackUrl** que representa a URL de retorno de chamada da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="42d41-107">This cmdlet returns a **CallbackUrl** object that represents the integration account callback URL.</span></span>
<span data-ttu-id="42d41-108">Especifique o nome da conta de integração e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="42d41-108">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="42d41-109">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="42d41-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="42d41-110">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="42d41-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="42d41-111">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="42d41-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="42d41-112">Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="42d41-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="42d41-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="42d41-113">EXAMPLES</span></span>

### <span data-ttu-id="42d41-114">Exemplo 1: Obter uma URL de retorno de chamada de conta de integração</span><span class="sxs-lookup"><span data-stu-id="42d41-114">Example 1: Get an integration account callback URL</span></span>
```
PS C:\>Get-AzIntegrationAccountCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -NotAfter "03/25/2016 18:23:22"
CallBackUrl : https://<baseurl>/integrationAccounts/8811f0155a364b5e9618ba28f7180601?api-version=2015-08-01-preview&se=2016-03
              -25T18%3A23%3A22.0000000Z&sp=%2F%2Fread&sv=1.0&sig=<value>
```

<span data-ttu-id="42d41-115">Este comando obtém uma URL de retorno de chamada de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="42d41-115">This command gets an integration account callback URL.</span></span>

## <span data-ttu-id="42d41-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="42d41-116">PARAMETERS</span></span>

### <span data-ttu-id="42d41-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42d41-117">-DefaultProfile</span></span>
<span data-ttu-id="42d41-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="42d41-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42d41-119">-Name</span><span class="sxs-lookup"><span data-stu-id="42d41-119">-Name</span></span>
<span data-ttu-id="42d41-120">Especifica o nome de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="42d41-120">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42d41-121">-NotAfter</span><span class="sxs-lookup"><span data-stu-id="42d41-121">-NotAfter</span></span>
<span data-ttu-id="42d41-122">Especifica a data de expiração para a URL de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="42d41-122">Specifies the expiry date for the callback URL.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42d41-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42d41-123">-ResourceGroupName</span></span>
<span data-ttu-id="42d41-124">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="42d41-124">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42d41-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42d41-125">CommonParameters</span></span>
<span data-ttu-id="42d41-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42d41-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42d41-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42d41-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42d41-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="42d41-128">INPUTS</span></span>

### <span data-ttu-id="42d41-129">System.String</span><span class="sxs-lookup"><span data-stu-id="42d41-129">System.String</span></span>

## <span data-ttu-id="42d41-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="42d41-130">OUTPUTS</span></span>

### <span data-ttu-id="42d41-131">Microsoft.Azure.Management.Logic.Models.CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="42d41-131">Microsoft.Azure.Management.Logic.Models.CallbackUrl</span></span>

## <span data-ttu-id="42d41-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="42d41-132">NOTES</span></span>

## <span data-ttu-id="42d41-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="42d41-133">RELATED LINKS</span></span>

[<span data-ttu-id="42d41-134">Get-AzLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="42d41-134">Get-AzLogicAppTriggerCallbackUrl</span></span>](./Get-AzLogicAppTriggerCallbackUrl.md)


