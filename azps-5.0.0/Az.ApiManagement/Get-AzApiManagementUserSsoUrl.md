---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
ms.openlocfilehash: be30497c444d90b9239b5dc3dcd351fbe9a63f0b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116461"
---
# <span data-ttu-id="454ff-101">Get-AzApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="454ff-101">Get-AzApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="454ff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="454ff-102">SYNOPSIS</span></span>
<span data-ttu-id="454ff-103">Gera uma URL de SSO para um usuário.</span><span class="sxs-lookup"><span data-stu-id="454ff-103">Generates an SSO URL for a user.</span></span>

## <span data-ttu-id="454ff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="454ff-104">SYNTAX</span></span>

```
Get-AzApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="454ff-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="454ff-105">DESCRIPTION</span></span>
<span data-ttu-id="454ff-106">O cmdlet **Get-AzApiManagementUserSsoUrl** gera uma URL de logon único (SSO) para um usuário.</span><span class="sxs-lookup"><span data-stu-id="454ff-106">The **Get-AzApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="454ff-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="454ff-107">EXAMPLES</span></span>

### <span data-ttu-id="454ff-108">Exemplo 1: obter a URL do SSO de um usuário</span><span class="sxs-lookup"><span data-stu-id="454ff-108">Example 1: Get a user's SSO URL</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="454ff-109">Esse comando obtém a URL de SSO de um usuário.</span><span class="sxs-lookup"><span data-stu-id="454ff-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="454ff-110">OS</span><span class="sxs-lookup"><span data-stu-id="454ff-110">PARAMETERS</span></span>

### <span data-ttu-id="454ff-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="454ff-111">-Context</span></span>
<span data-ttu-id="454ff-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="454ff-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="454ff-113">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="454ff-113">This parameter is required.</span></span>

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

### <span data-ttu-id="454ff-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="454ff-114">-DefaultProfile</span></span>
<span data-ttu-id="454ff-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="454ff-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="454ff-116">-UserId</span><span class="sxs-lookup"><span data-stu-id="454ff-116">-UserId</span></span>
<span data-ttu-id="454ff-117">Especifica uma ID de usuário.</span><span class="sxs-lookup"><span data-stu-id="454ff-117">Specifies a user ID.</span></span>
<span data-ttu-id="454ff-118">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="454ff-118">This parameter is required.</span></span>

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

### <span data-ttu-id="454ff-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="454ff-119">CommonParameters</span></span>
<span data-ttu-id="454ff-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="454ff-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="454ff-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="454ff-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="454ff-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="454ff-122">INPUTS</span></span>

### <span data-ttu-id="454ff-123">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="454ff-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="454ff-124">System. String</span><span class="sxs-lookup"><span data-stu-id="454ff-124">System.String</span></span>

## <span data-ttu-id="454ff-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="454ff-125">OUTPUTS</span></span>

### <span data-ttu-id="454ff-126">System. String</span><span class="sxs-lookup"><span data-stu-id="454ff-126">System.String</span></span>

## <span data-ttu-id="454ff-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="454ff-127">NOTES</span></span>

## <span data-ttu-id="454ff-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="454ff-128">RELATED LINKS</span></span>

[<span data-ttu-id="454ff-129">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="454ff-129">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


