---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
ms.openlocfilehash: b4c89a1f0da5e4ce07d9d2174fce031365e09cb4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888770"
---
# <span data-ttu-id="e4bee-101">Get-AzApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="e4bee-101">Get-AzApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="e4bee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4bee-102">SYNOPSIS</span></span>
<span data-ttu-id="e4bee-103">Gera uma URL de SSO para um usuário.</span><span class="sxs-lookup"><span data-stu-id="e4bee-103">Generates an SSO URL for a user.</span></span>

## <span data-ttu-id="e4bee-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e4bee-104">SYNTAX</span></span>

```
Get-AzApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4bee-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e4bee-105">DESCRIPTION</span></span>
<span data-ttu-id="e4bee-106">O cmdlet **Get-AzApiManagementUserSsoUrl** gera uma URL de entrada única (SSO) para um usuário.</span><span class="sxs-lookup"><span data-stu-id="e4bee-106">The **Get-AzApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="e4bee-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4bee-107">EXAMPLES</span></span>

### <span data-ttu-id="e4bee-108">Exemplo 1: Obter a URL do SSO de um usuário</span><span class="sxs-lookup"><span data-stu-id="e4bee-108">Example 1: Get a user's SSO URL</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="e4bee-109">Esse comando obtém a URL de SSO de um usuário.</span><span class="sxs-lookup"><span data-stu-id="e4bee-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="e4bee-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e4bee-110">PARAMETERS</span></span>

### <span data-ttu-id="e4bee-111">-Context</span><span class="sxs-lookup"><span data-stu-id="e4bee-111">-Context</span></span>
<span data-ttu-id="e4bee-112">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="e4bee-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="e4bee-113">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="e4bee-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4bee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4bee-114">-DefaultProfile</span></span>
<span data-ttu-id="e4bee-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e4bee-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4bee-116">-UserId</span><span class="sxs-lookup"><span data-stu-id="e4bee-116">-UserId</span></span>
<span data-ttu-id="e4bee-117">Especifica uma ID de usuário.</span><span class="sxs-lookup"><span data-stu-id="e4bee-117">Specifies a user ID.</span></span>
<span data-ttu-id="e4bee-118">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="e4bee-118">This parameter is required.</span></span>

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

### <span data-ttu-id="e4bee-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4bee-119">CommonParameters</span></span>
<span data-ttu-id="e4bee-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4bee-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4bee-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4bee-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4bee-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e4bee-122">INPUTS</span></span>

### <span data-ttu-id="e4bee-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e4bee-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e4bee-124">System.String</span><span class="sxs-lookup"><span data-stu-id="e4bee-124">System.String</span></span>

## <span data-ttu-id="e4bee-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e4bee-125">OUTPUTS</span></span>

### <span data-ttu-id="e4bee-126">System.String</span><span class="sxs-lookup"><span data-stu-id="e4bee-126">System.String</span></span>

## <span data-ttu-id="e4bee-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="e4bee-127">NOTES</span></span>

## <span data-ttu-id="e4bee-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4bee-128">RELATED LINKS</span></span>

[<span data-ttu-id="e4bee-129">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="e4bee-129">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


