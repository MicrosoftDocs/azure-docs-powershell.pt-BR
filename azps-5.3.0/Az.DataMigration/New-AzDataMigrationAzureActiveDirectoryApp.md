---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationAzureActiveDirectoryApp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
ms.openlocfilehash: 8eec47c703290047b51ce38e97391500a9f27d74
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272949"
---
# <span data-ttu-id="67f7b-101">New-AzDataMigrationAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="67f7b-101">New-AzDataMigrationAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="67f7b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="67f7b-102">SYNOPSIS</span></span>
<span data-ttu-id="67f7b-103">Crie um novo exemplo de aplicativo do Azure ActiveDirectory para migração de dados de instância.</span><span class="sxs-lookup"><span data-stu-id="67f7b-103">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="67f7b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="67f7b-104">SYNTAX</span></span>

```
New-AzDataMigrationAzureActiveDirectoryApp -ApplicationId <String> -AppKey <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67f7b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="67f7b-105">DESCRIPTION</span></span>
<span data-ttu-id="67f7b-106">Crie um novo exemplo de aplicativo do Azure ActiveDirectory para migração de dados de instância.</span><span class="sxs-lookup"><span data-stu-id="67f7b-106">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="67f7b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="67f7b-107">EXAMPLES</span></span>

### <span data-ttu-id="67f7b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="67f7b-108">Example 1</span></span>
```powershell
PS C:\> $secpasswd = ConvertTo-SecureString "Your Secret Key Here" -AsPlainText -Force
C:\> New-AzDmsAadApp -ApplicationId "Your AppId/Service Principal ID here" -AppKey $secpasswd
```
<span data-ttu-id="67f7b-109">ApplicationId: "a AppId/ID da entidade do serviço aqui" AppKey: System. Security. SecureString Tenantid: "ID do locatário"</span><span class="sxs-lookup"><span data-stu-id="67f7b-109">ApplicationId : "Your AppId/Service Principal Id here" AppKey        : System.Security.SecureString TenantId      : "Tenant Id"</span></span>

## <span data-ttu-id="67f7b-110">OS</span><span class="sxs-lookup"><span data-stu-id="67f7b-110">PARAMETERS</span></span>

### <span data-ttu-id="67f7b-111">-AppKey</span><span class="sxs-lookup"><span data-stu-id="67f7b-111">-AppKey</span></span>
<span data-ttu-id="67f7b-112">Chave do Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="67f7b-112">Azure Active Directory Key</span></span>

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

### <span data-ttu-id="67f7b-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="67f7b-113">-ApplicationId</span></span>
<span data-ttu-id="67f7b-114">ID de aplicativo do Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="67f7b-114">Azure Active Directory Application Id</span></span>

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

### <span data-ttu-id="67f7b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67f7b-115">-DefaultProfile</span></span>
<span data-ttu-id="67f7b-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="67f7b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67f7b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67f7b-117">CommonParameters</span></span>
<span data-ttu-id="67f7b-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67f7b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="67f7b-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67f7b-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67f7b-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="67f7b-120">INPUTS</span></span>

### <span data-ttu-id="67f7b-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="67f7b-121">None</span></span>

## <span data-ttu-id="67f7b-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="67f7b-122">OUTPUTS</span></span>

### <span data-ttu-id="67f7b-123">Microsoft. Azure. Commands. datamigration. Models. PSAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="67f7b-123">Microsoft.Azure.Commands.DataMigration.Models.PSAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="67f7b-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="67f7b-124">NOTES</span></span>

## <span data-ttu-id="67f7b-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="67f7b-125">RELATED LINKS</span></span>
