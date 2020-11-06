---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
ms.openlocfilehash: d405dc21719abc1aec5767f4d1b89a938b79eaf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428323"
---
# <span data-ttu-id="96c51-101">Add-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="96c51-101">Add-AzureRmApiManagementUserToGroup</span></span>

## <span data-ttu-id="96c51-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="96c51-102">SYNOPSIS</span></span>
<span data-ttu-id="96c51-103">Adiciona um usuário a um grupo.</span><span class="sxs-lookup"><span data-stu-id="96c51-103">Adds a user to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96c51-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="96c51-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96c51-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="96c51-105">DESCRIPTION</span></span>
<span data-ttu-id="96c51-106">O cmdlet **Add-AzureRmApiManagementUserToGroup** adiciona um usuário a um grupo.</span><span class="sxs-lookup"><span data-stu-id="96c51-106">The **Add-AzureRmApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="96c51-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="96c51-107">EXAMPLES</span></span>

### <span data-ttu-id="96c51-108">Exemplo 1: adicionar um usuário a um grupo</span><span class="sxs-lookup"><span data-stu-id="96c51-108">Example 1: Add a user to a group</span></span>
```
PS C:\>Add-AzureRmApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="96c51-109">Esse comando adiciona um usuário existente a um grupo existente.</span><span class="sxs-lookup"><span data-stu-id="96c51-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="96c51-110">OS</span><span class="sxs-lookup"><span data-stu-id="96c51-110">PARAMETERS</span></span>

### <span data-ttu-id="96c51-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="96c51-111">-Context</span></span>
<span data-ttu-id="96c51-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="96c51-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="96c51-113">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="96c51-113">This parameter is required.</span></span>

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

### <span data-ttu-id="96c51-114">-GroupId</span><span class="sxs-lookup"><span data-stu-id="96c51-114">-GroupId</span></span>
<span data-ttu-id="96c51-115">Especifica a ID do grupo.</span><span class="sxs-lookup"><span data-stu-id="96c51-115">Specifies the group ID.</span></span>
<span data-ttu-id="96c51-116">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="96c51-116">This parameter is required.</span></span>

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

### <span data-ttu-id="96c51-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96c51-117">-PassThru</span></span>
<span data-ttu-id="96c51-118">PassThru</span><span class="sxs-lookup"><span data-stu-id="96c51-118">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96c51-119">-UserId</span><span class="sxs-lookup"><span data-stu-id="96c51-119">-UserId</span></span>
<span data-ttu-id="96c51-120">Especifica a ID de usuário.</span><span class="sxs-lookup"><span data-stu-id="96c51-120">Specifies the user ID.</span></span>
<span data-ttu-id="96c51-121">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="96c51-121">This parameter is required.</span></span>

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

### <span data-ttu-id="96c51-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96c51-122">-DefaultProfile</span></span>
<span data-ttu-id="96c51-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="96c51-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96c51-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96c51-124">CommonParameters</span></span>
<span data-ttu-id="96c51-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96c51-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96c51-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96c51-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96c51-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="96c51-127">INPUTS</span></span>

## <span data-ttu-id="96c51-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="96c51-128">OUTPUTS</span></span>

### <span data-ttu-id="96c51-129">Booliana</span><span class="sxs-lookup"><span data-stu-id="96c51-129">Boolean</span></span>

## <span data-ttu-id="96c51-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="96c51-130">NOTES</span></span>

## <span data-ttu-id="96c51-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="96c51-131">RELATED LINKS</span></span>

[<span data-ttu-id="96c51-132">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="96c51-132">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="96c51-133">Remove-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="96c51-133">Remove-AzureRmApiManagementUserFromGroup</span></span>](./Remove-AzureRmApiManagementUserFromGroup.md)


