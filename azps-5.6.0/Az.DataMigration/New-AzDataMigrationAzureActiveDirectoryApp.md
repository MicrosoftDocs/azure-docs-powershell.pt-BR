---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationAzureActiveDirectoryApp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
ms.openlocfilehash: 6fa598b792d04d8223aafdb39405a69ada6e5915
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887216"
---
# <span data-ttu-id="a928a-101">New-AzDataMigrationAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="a928a-101">New-AzDataMigrationAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="a928a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a928a-102">SYNOPSIS</span></span>
<span data-ttu-id="a928a-103">Crie uma nova instância Detalhes do Aplicativo DataMigration do Azure ActiveDirectory.</span><span class="sxs-lookup"><span data-stu-id="a928a-103">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="a928a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a928a-104">SYNTAX</span></span>

```
New-AzDataMigrationAzureActiveDirectoryApp -ApplicationId <String> -AppKey <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a928a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a928a-105">DESCRIPTION</span></span>
<span data-ttu-id="a928a-106">Crie uma nova instância Detalhes do Aplicativo DataMigration do Azure ActiveDirectory.</span><span class="sxs-lookup"><span data-stu-id="a928a-106">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="a928a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a928a-107">EXAMPLES</span></span>

### <span data-ttu-id="a928a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a928a-108">Example 1</span></span>
```powershell
PS C:\> $secpasswd = ConvertTo-SecureString "Your Secret Key Here" -AsPlainText -Force
C:\> New-AzDmsAadApp -ApplicationId "Your AppId/Service Principal ID here" -AppKey $secpasswd
```
<span data-ttu-id="a928a-109">ApplicationId : "Sua Id da Entidade de Serviço/AppId aqui" AppKey : System.Security.SecureString TenantId : "Id do locatário"</span><span class="sxs-lookup"><span data-stu-id="a928a-109">ApplicationId : "Your AppId/Service Principal Id here" AppKey        : System.Security.SecureString TenantId      : "Tenant Id"</span></span>

## <span data-ttu-id="a928a-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a928a-110">PARAMETERS</span></span>

### <span data-ttu-id="a928a-111">-AppKey</span><span class="sxs-lookup"><span data-stu-id="a928a-111">-AppKey</span></span>
<span data-ttu-id="a928a-112">Chave do Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="a928a-112">Azure Active Directory Key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: Key

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a928a-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a928a-113">-ApplicationId</span></span>
<span data-ttu-id="a928a-114">ID de aplicativo do Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="a928a-114">Azure Active Directory Application Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a928a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a928a-115">-DefaultProfile</span></span>
<span data-ttu-id="a928a-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a928a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a928a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a928a-117">CommonParameters</span></span>
<span data-ttu-id="a928a-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a928a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a928a-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a928a-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a928a-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a928a-120">INPUTS</span></span>

### <span data-ttu-id="a928a-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a928a-121">None</span></span>

## <span data-ttu-id="a928a-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a928a-122">OUTPUTS</span></span>

### <span data-ttu-id="a928a-123">Microsoft.Azure.Commands.DataMigration.Models.PSAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="a928a-123">Microsoft.Azure.Commands.DataMigration.Models.PSAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="a928a-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="a928a-124">NOTES</span></span>

## <span data-ttu-id="a928a-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a928a-125">RELATED LINKS</span></span>
