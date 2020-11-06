---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppDatabaseBackupSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppDatabaseBackupSetting.md
ms.openlocfilehash: d8662f0a3f9ff10fccd9d38a2d5397bf32ea6b8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610687"
---
# <span data-ttu-id="4dae9-101">New-AzureRmWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="4dae9-101">New-AzureRmWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="4dae9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4dae9-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4dae9-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4dae9-103">SYNTAX</span></span>

```
New-AzureRmWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4dae9-104">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4dae9-104">DESCRIPTION</span></span>
<span data-ttu-id="4dae9-105">O cmdlet **New-AzureRmWebAppDatabaseBackupSetting** cria uma nova configuração de backup do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="4dae9-105">The **New-AzureRmWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="4dae9-106">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4dae9-106">EXAMPLES</span></span>

### <span data-ttu-id="4dae9-107">1:</span><span class="sxs-lookup"><span data-stu-id="4dae9-107">1:</span></span>
```
PS C:\> New-AzureRmWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="4dae9-108">Cria uma configuração de backup de banco de dados (cadeia de conexão) do tipo sqlazure para o aplicativo especificado ContosoWebApp que está dentro do grupo de recursos-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="4dae9-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="4dae9-109">OS</span><span class="sxs-lookup"><span data-stu-id="4dae9-109">PARAMETERS</span></span>

### <span data-ttu-id="4dae9-110">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="4dae9-110">-ConnectionString</span></span>
<span data-ttu-id="4dae9-111">Cadeia de conexão</span><span class="sxs-lookup"><span data-stu-id="4dae9-111">Connection String</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dae9-112">-ConnectionStringname</span><span class="sxs-lookup"><span data-stu-id="4dae9-112">-ConnectionStringName</span></span>
<span data-ttu-id="4dae9-113">Nome da cadeia de conexão</span><span class="sxs-lookup"><span data-stu-id="4dae9-113">Connection String Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dae9-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="4dae9-114">-DatabaseType</span></span>
<span data-ttu-id="4dae9-115">Tipo de banco de dados (por exemplo, "sqlazure" ou "MySql")</span><span class="sxs-lookup"><span data-stu-id="4dae9-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dae9-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="4dae9-116">-Name</span></span>
<span data-ttu-id="4dae9-117">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="4dae9-117">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dae9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dae9-118">-DefaultProfile</span></span>
<span data-ttu-id="4dae9-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4dae9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4dae9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dae9-120">CommonParameters</span></span>
<span data-ttu-id="4dae9-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dae9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dae9-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dae9-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dae9-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4dae9-123">INPUTS</span></span>

## <span data-ttu-id="4dae9-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4dae9-124">OUTPUTS</span></span>

### <span data-ttu-id="4dae9-125">Microsoft. Azure. Management. WebSites. Models. DatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="4dae9-125">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="4dae9-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4dae9-126">NOTES</span></span>

## <span data-ttu-id="4dae9-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4dae9-127">RELATED LINKS</span></span>

