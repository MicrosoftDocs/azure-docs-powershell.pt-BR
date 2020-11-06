---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationconnectioninfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
ms.openlocfilehash: aca970403d7ef85733d808c8e21df3d0b2066f9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428217"
---
# <span data-ttu-id="9a64d-101">New-AzureRmDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="9a64d-101">New-AzureRmDataMigrationConnectionInfo</span></span>

## <span data-ttu-id="9a64d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9a64d-102">SYNOPSIS</span></span>
<span data-ttu-id="9a64d-103">Cria um novo objeto de informações de conexão especificando o tipo e o nome do servidor para a conexão.</span><span class="sxs-lookup"><span data-stu-id="9a64d-103">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a64d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9a64d-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="9a64d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9a64d-105">DESCRIPTION</span></span>
<span data-ttu-id="9a64d-106">O cmdlet New-AzureRmDataMigrationConnectionInfo cria um objeto de informações de conexão novo especificando o tipo de servidor para conexão.</span><span class="sxs-lookup"><span data-stu-id="9a64d-106">The New-AzureRmDataMigrationConnectionInfo cmdlet creates new a Connection Info object specifying the server type for connection.</span></span> 



## <span data-ttu-id="9a64d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9a64d-107">EXAMPLES</span></span>

### <span data-ttu-id="9a64d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9a64d-108">Example 1</span></span>
```
PS C:\> New-AzureRmDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```
<span data-ttu-id="9a64d-109">O exemplo anterior cria um novo objeto de informações de conexão fornecendo SQL como parâmetro ServerType.</span><span class="sxs-lookup"><span data-stu-id="9a64d-109">The preceding example creates a new Connection Info object providing SQL as ServerType parameter.</span></span>


## <span data-ttu-id="9a64d-110">OS</span><span class="sxs-lookup"><span data-stu-id="9a64d-110">PARAMETERS</span></span>

### <span data-ttu-id="9a64d-111">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9a64d-111">-Confirm</span></span>
<span data-ttu-id="9a64d-112">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a64d-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="9a64d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a64d-113">-DefaultProfile</span></span>
<span data-ttu-id="9a64d-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9a64d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a64d-115">-ServerType</span><span class="sxs-lookup"><span data-stu-id="9a64d-115">-ServerType</span></span>
<span data-ttu-id="9a64d-116">Enum que descreve o tipo de servidor ao qual se conectar.</span><span class="sxs-lookup"><span data-stu-id="9a64d-116">Enum that describes server type to connect to.</span></span> <span data-ttu-id="9a64d-117">Os valores atualmente com suporte são SQL Server e SQLDB para SQL Azure Database.</span><span class="sxs-lookup"><span data-stu-id="9a64d-117">Currently supported values are SQL for SQL Server and SQLDB for SQL Azure Database.</span></span> 

```yaml
Type: ServerTypeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: SQL, SQLDB

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="9a64d-118">-AuthType</span><span class="sxs-lookup"><span data-stu-id="9a64d-118">-AuthType</span></span>
<span data-ttu-id="9a64d-119">Tipo de autenticação a ser usado para conexão.</span><span class="sxs-lookup"><span data-stu-id="9a64d-119">Authentication type to use for connection.</span></span> <span data-ttu-id="9a64d-120">Os valores possíveis são sqlauthentication e WindowsAuthentication</span><span class="sxs-lookup"><span data-stu-id="9a64d-120">Possible values are SqlAuthentication and WindowsAuthentication</span></span>

```yaml
Type: AuthenticationTypeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a64d-121">-DataSource</span><span class="sxs-lookup"><span data-stu-id="9a64d-121">-DataSource</span></span>
<span data-ttu-id="9a64d-122">Servidor address\name ao qual se conectar.</span><span class="sxs-lookup"><span data-stu-id="9a64d-122">Server address\name to connect to.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a64d-123">-TrustServerCertificate</span><span class="sxs-lookup"><span data-stu-id="9a64d-123">-TrustServerCertificate</span></span>
<span data-ttu-id="9a64d-124">Booliano que indica a garantia de que a criptografia ocorre.</span><span class="sxs-lookup"><span data-stu-id="9a64d-124">Boolean indicating to guarantee that encryption takes place.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a64d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a64d-125">-WhatIf</span></span>
<span data-ttu-id="9a64d-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9a64d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a64d-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9a64d-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```





## <span data-ttu-id="9a64d-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9a64d-128">INPUTS</span></span>

### <span data-ttu-id="9a64d-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9a64d-129">None</span></span>


## <span data-ttu-id="9a64d-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9a64d-130">OUTPUTS</span></span>

### <span data-ttu-id="9a64d-131">Microsoft. Azure. Management. datamigration. Models. ConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="9a64d-131">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span></span>


## <span data-ttu-id="9a64d-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9a64d-132">NOTES</span></span>

## <span data-ttu-id="9a64d-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9a64d-133">RELATED LINKS</span></span>

