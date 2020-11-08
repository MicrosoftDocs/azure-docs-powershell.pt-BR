---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 4813EE2B-16C4-4716-B6DD-9447A0B46F3D
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountcallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCallbackUrl.md
ms.openlocfilehash: 91a61935552258e5ca52ded6e05729deecaf5665
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124598"
---
# <span data-ttu-id="af15b-101">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="af15b-101">Get-AzIntegrationAccountCallbackUrl</span></span>

## <span data-ttu-id="af15b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="af15b-102">SYNOPSIS</span></span>
<span data-ttu-id="af15b-103">Obtém uma URL de retorno de chamada de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="af15b-103">Gets an integration account callback URL.</span></span>

## <span data-ttu-id="af15b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af15b-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountCallbackUrl -ResourceGroupName <String> -Name <String> [-NotAfter <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af15b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="af15b-105">DESCRIPTION</span></span>
<span data-ttu-id="af15b-106">O cmdlet **Get-AzIntegrationAccountCallbackUrl** Obtém uma URL de retorno de chamada de conta de integração de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="af15b-106">The **Get-AzIntegrationAccountCallbackUrl** cmdlet gets an integration account callback URL from a resource group.</span></span>
<span data-ttu-id="af15b-107">Esse cmdlet retorna um objeto **CallbackUrl** que representa a URL de retorno de chamada da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="af15b-107">This cmdlet returns a **CallbackUrl** object that represents the integration account callback URL.</span></span>
<span data-ttu-id="af15b-108">Especifique o nome da conta de integração e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="af15b-108">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="af15b-109">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="af15b-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="af15b-110">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="af15b-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="af15b-111">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="af15b-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="af15b-112">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="af15b-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="af15b-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="af15b-113">EXAMPLES</span></span>

### <span data-ttu-id="af15b-114">Exemplo 1: obter uma URL de retorno de chamada de conta de integração</span><span class="sxs-lookup"><span data-stu-id="af15b-114">Example 1: Get an integration account callback URL</span></span>
```
PS C:\>Get-AzIntegrationAccountCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -NotAfter "03/25/2016 18:23:22"
CallBackUrl : https://<baseurl>/integrationAccounts/8811f0155a364b5e9618ba28f7180601?api-version=2015-08-01-preview&se=2016-03
              -25T18%3A23%3A22.0000000Z&sp=%2F%2Fread&sv=1.0&sig=<value>
```

<span data-ttu-id="af15b-115">Esse comando obtém uma URL de retorno de chamada de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="af15b-115">This command gets an integration account callback URL.</span></span>

## <span data-ttu-id="af15b-116">OS</span><span class="sxs-lookup"><span data-stu-id="af15b-116">PARAMETERS</span></span>

### <span data-ttu-id="af15b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af15b-117">-DefaultProfile</span></span>
<span data-ttu-id="af15b-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="af15b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af15b-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="af15b-119">-Name</span></span>
<span data-ttu-id="af15b-120">Especifica o nome de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="af15b-120">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="af15b-121">-Não depois</span><span class="sxs-lookup"><span data-stu-id="af15b-121">-NotAfter</span></span>
<span data-ttu-id="af15b-122">Especifica a data de vencimento para a URL de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="af15b-122">Specifies the expiry date for the callback URL.</span></span>

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

### <span data-ttu-id="af15b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af15b-123">-ResourceGroupName</span></span>
<span data-ttu-id="af15b-124">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="af15b-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="af15b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af15b-125">CommonParameters</span></span>
<span data-ttu-id="af15b-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af15b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af15b-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af15b-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af15b-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="af15b-128">INPUTS</span></span>

### <span data-ttu-id="af15b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="af15b-129">System.String</span></span>

## <span data-ttu-id="af15b-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="af15b-130">OUTPUTS</span></span>

### <span data-ttu-id="af15b-131">Microsoft. Azure. Management. Logic. Models. CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="af15b-131">Microsoft.Azure.Management.Logic.Models.CallbackUrl</span></span>

## <span data-ttu-id="af15b-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="af15b-132">NOTES</span></span>

## <span data-ttu-id="af15b-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af15b-133">RELATED LINKS</span></span>

[<span data-ttu-id="af15b-134">Get-AzLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="af15b-134">Get-AzLogicAppTriggerCallbackUrl</span></span>](./Get-AzLogicAppTriggerCallbackUrl.md)


