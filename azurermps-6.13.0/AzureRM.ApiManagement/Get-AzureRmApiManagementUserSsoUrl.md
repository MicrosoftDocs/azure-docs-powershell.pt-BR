---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
ms.openlocfilehash: 485150470bce308d3ab6d1a9a70eabd887abab09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431471"
---
# <span data-ttu-id="34180-101">Get-AzureRmApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="34180-101">Get-AzureRmApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="34180-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="34180-102">SYNOPSIS</span></span>
<span data-ttu-id="34180-103">Gera uma URL de SSO para um usuário.</span><span class="sxs-lookup"><span data-stu-id="34180-103">Generates an SSO URL for a user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34180-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="34180-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34180-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="34180-105">DESCRIPTION</span></span>
<span data-ttu-id="34180-106">O cmdlet **Get-AzureRmApiManagementUserSsoUrl** gera uma URL de logon único (SSO) para um usuário.</span><span class="sxs-lookup"><span data-stu-id="34180-106">The **Get-AzureRmApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="34180-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="34180-107">EXAMPLES</span></span>

### <span data-ttu-id="34180-108">Exemplo 1: obter a URL do SSO de um usuário</span><span class="sxs-lookup"><span data-stu-id="34180-108">Example 1: Get a user's SSO URL</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="34180-109">Esse comando obtém a URL de SSO de um usuário.</span><span class="sxs-lookup"><span data-stu-id="34180-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="34180-110">OS</span><span class="sxs-lookup"><span data-stu-id="34180-110">PARAMETERS</span></span>

### <span data-ttu-id="34180-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="34180-111">-Context</span></span>
<span data-ttu-id="34180-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="34180-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="34180-113">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="34180-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34180-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34180-114">-DefaultProfile</span></span>
<span data-ttu-id="34180-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="34180-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34180-116">-UserId</span><span class="sxs-lookup"><span data-stu-id="34180-116">-UserId</span></span>
<span data-ttu-id="34180-117">Especifica uma ID de usuário.</span><span class="sxs-lookup"><span data-stu-id="34180-117">Specifies a user ID.</span></span>
<span data-ttu-id="34180-118">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="34180-118">This parameter is required.</span></span>

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

### <span data-ttu-id="34180-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34180-119">CommonParameters</span></span>
<span data-ttu-id="34180-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34180-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34180-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34180-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34180-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="34180-122">INPUTS</span></span>

### <span data-ttu-id="34180-123">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="34180-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="34180-124">System. String</span><span class="sxs-lookup"><span data-stu-id="34180-124">System.String</span></span>

## <span data-ttu-id="34180-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="34180-125">OUTPUTS</span></span>

### <span data-ttu-id="34180-126">System. String</span><span class="sxs-lookup"><span data-stu-id="34180-126">System.String</span></span>

## <span data-ttu-id="34180-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="34180-127">NOTES</span></span>

## <span data-ttu-id="34180-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="34180-128">RELATED LINKS</span></span>

[<span data-ttu-id="34180-129">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="34180-129">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)


