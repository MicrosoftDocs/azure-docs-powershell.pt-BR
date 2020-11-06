---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSsoToken.md
ms.openlocfilehash: e0bce4f579b2000bc970e35ceb03da03fdffb211
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426513"
---
# <span data-ttu-id="36016-101">Get-AzureRmApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="36016-101">Get-AzureRmApiManagementSsoToken</span></span>

## <span data-ttu-id="36016-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="36016-102">SYNOPSIS</span></span>
<span data-ttu-id="36016-103">Obtém um link com um token de SSO para um portal de gerenciamento implantado de um serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="36016-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36016-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36016-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36016-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="36016-105">DESCRIPTION</span></span>
<span data-ttu-id="36016-106">O cmdlet **Get-AzureRmApiManagementSsoToken** retorna um link (URL) que contém um token de logon único (SSO) para um portal de gerenciamento implantado de um serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="36016-106">The **Get-AzureRmApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="36016-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="36016-107">EXAMPLES</span></span>

### <span data-ttu-id="36016-108">Exemplo 1: obter o token de SSO de um serviço de gerenciamento de API</span><span class="sxs-lookup"><span data-stu-id="36016-108">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzureRmApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="36016-109">Esse comando obtém o token de SSO de um serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="36016-109">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="36016-110">OS</span><span class="sxs-lookup"><span data-stu-id="36016-110">PARAMETERS</span></span>

### <span data-ttu-id="36016-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36016-111">-DefaultProfile</span></span>
<span data-ttu-id="36016-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="36016-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36016-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="36016-113">-Name</span></span>
<span data-ttu-id="36016-114">Especifica o nome da instância de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="36016-114">Specifies the name of the API Management instance.</span></span>

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

### <span data-ttu-id="36016-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36016-115">-ResourceGroupName</span></span>
<span data-ttu-id="36016-116">Especifica o nome do grupo de recursos sob o qual existe gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="36016-116">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="36016-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36016-117">CommonParameters</span></span>
<span data-ttu-id="36016-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36016-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36016-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36016-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36016-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="36016-120">INPUTS</span></span>

### <span data-ttu-id="36016-121">System. String</span><span class="sxs-lookup"><span data-stu-id="36016-121">System.String</span></span>

## <span data-ttu-id="36016-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="36016-122">OUTPUTS</span></span>

### <span data-ttu-id="36016-123">System. String</span><span class="sxs-lookup"><span data-stu-id="36016-123">System.String</span></span>

## <span data-ttu-id="36016-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="36016-124">NOTES</span></span>

## <span data-ttu-id="36016-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="36016-125">RELATED LINKS</span></span>

[<span data-ttu-id="36016-126">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="36016-126">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)


