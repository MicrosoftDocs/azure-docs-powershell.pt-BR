---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
ms.openlocfilehash: be30497c444d90b9239b5dc3dcd351fbe9a63f0b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258035"
---
# <span data-ttu-id="f23c3-101">Get-AzApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="f23c3-101">Get-AzApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="f23c3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f23c3-102">SYNOPSIS</span></span>
<span data-ttu-id="f23c3-103">Gera uma URL de SSO para um usuário.</span><span class="sxs-lookup"><span data-stu-id="f23c3-103">Generates an SSO URL for a user.</span></span>

## <span data-ttu-id="f23c3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f23c3-104">SYNTAX</span></span>

```
Get-AzApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f23c3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f23c3-105">DESCRIPTION</span></span>
<span data-ttu-id="f23c3-106">O cmdlet **Get-AzApiManagementUserSsoUrl** gera uma URL de logon único (SSO) para um usuário.</span><span class="sxs-lookup"><span data-stu-id="f23c3-106">The **Get-AzApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="f23c3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f23c3-107">EXAMPLES</span></span>

### <span data-ttu-id="f23c3-108">Exemplo 1: obter a URL do SSO de um usuário</span><span class="sxs-lookup"><span data-stu-id="f23c3-108">Example 1: Get a user's SSO URL</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="f23c3-109">Esse comando obtém a URL de SSO de um usuário.</span><span class="sxs-lookup"><span data-stu-id="f23c3-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="f23c3-110">OS</span><span class="sxs-lookup"><span data-stu-id="f23c3-110">PARAMETERS</span></span>

### <span data-ttu-id="f23c3-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="f23c3-111">-Context</span></span>
<span data-ttu-id="f23c3-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="f23c3-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="f23c3-113">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="f23c3-113">This parameter is required.</span></span>

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

### <span data-ttu-id="f23c3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f23c3-114">-DefaultProfile</span></span>
<span data-ttu-id="f23c3-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f23c3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f23c3-116">-UserId</span><span class="sxs-lookup"><span data-stu-id="f23c3-116">-UserId</span></span>
<span data-ttu-id="f23c3-117">Especifica uma ID de usuário.</span><span class="sxs-lookup"><span data-stu-id="f23c3-117">Specifies a user ID.</span></span>
<span data-ttu-id="f23c3-118">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="f23c3-118">This parameter is required.</span></span>

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

### <span data-ttu-id="f23c3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f23c3-119">CommonParameters</span></span>
<span data-ttu-id="f23c3-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f23c3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f23c3-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f23c3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f23c3-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f23c3-122">INPUTS</span></span>

### <span data-ttu-id="f23c3-123">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f23c3-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f23c3-124">System. String</span><span class="sxs-lookup"><span data-stu-id="f23c3-124">System.String</span></span>

## <span data-ttu-id="f23c3-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f23c3-125">OUTPUTS</span></span>

### <span data-ttu-id="f23c3-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f23c3-126">System.String</span></span>

## <span data-ttu-id="f23c3-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f23c3-127">NOTES</span></span>

## <span data-ttu-id="f23c3-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f23c3-128">RELATED LINKS</span></span>

[<span data-ttu-id="f23c3-129">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f23c3-129">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


