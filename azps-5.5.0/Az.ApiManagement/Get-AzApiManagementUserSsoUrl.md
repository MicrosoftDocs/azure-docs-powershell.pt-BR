---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
ms.openlocfilehash: be30497c444d90b9239b5dc3dcd351fbe9a63f0b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110841"
---
# <span data-ttu-id="3619e-101">Get-AzApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="3619e-101">Get-AzApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="3619e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3619e-102">SYNOPSIS</span></span>
<span data-ttu-id="3619e-103">Gera uma URL de SSO para um usuário.</span><span class="sxs-lookup"><span data-stu-id="3619e-103">Generates an SSO URL for a user.</span></span>

## <span data-ttu-id="3619e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3619e-104">SYNTAX</span></span>

```
Get-AzApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3619e-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="3619e-105">DESCRIPTION</span></span>
<span data-ttu-id="3619e-106">O cmdlet **Get-AzApiManagementUserSsoUrl** gera uma URL de entrada única (SSO) para um usuário.</span><span class="sxs-lookup"><span data-stu-id="3619e-106">The **Get-AzApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="3619e-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3619e-107">EXAMPLES</span></span>

### <span data-ttu-id="3619e-108">Exemplo 1: Obter a URL de SSO de um usuário</span><span class="sxs-lookup"><span data-stu-id="3619e-108">Example 1: Get a user's SSO URL</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="3619e-109">Esse comando obtém a URL do SSO do usuário.</span><span class="sxs-lookup"><span data-stu-id="3619e-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="3619e-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3619e-110">PARAMETERS</span></span>

### <span data-ttu-id="3619e-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="3619e-111">-Context</span></span>
<span data-ttu-id="3619e-112">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="3619e-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="3619e-113">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="3619e-113">This parameter is required.</span></span>

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

### <span data-ttu-id="3619e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3619e-114">-DefaultProfile</span></span>
<span data-ttu-id="3619e-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="3619e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3619e-116">-UserId</span><span class="sxs-lookup"><span data-stu-id="3619e-116">-UserId</span></span>
<span data-ttu-id="3619e-117">Especifica uma ID de usuário.</span><span class="sxs-lookup"><span data-stu-id="3619e-117">Specifies a user ID.</span></span>
<span data-ttu-id="3619e-118">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="3619e-118">This parameter is required.</span></span>

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

### <span data-ttu-id="3619e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3619e-119">CommonParameters</span></span>
<span data-ttu-id="3619e-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3619e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3619e-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3619e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3619e-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="3619e-122">INPUTS</span></span>

### <span data-ttu-id="3619e-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3619e-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3619e-124">System.String</span><span class="sxs-lookup"><span data-stu-id="3619e-124">System.String</span></span>

## <span data-ttu-id="3619e-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="3619e-125">OUTPUTS</span></span>

### <span data-ttu-id="3619e-126">System.String</span><span class="sxs-lookup"><span data-stu-id="3619e-126">System.String</span></span>

## <span data-ttu-id="3619e-127">Notas</span><span class="sxs-lookup"><span data-stu-id="3619e-127">NOTES</span></span>

## <span data-ttu-id="3619e-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3619e-128">RELATED LINKS</span></span>

[<span data-ttu-id="3619e-129">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="3619e-129">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


