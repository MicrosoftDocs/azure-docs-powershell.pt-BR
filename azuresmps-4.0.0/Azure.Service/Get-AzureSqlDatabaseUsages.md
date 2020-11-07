---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 9953AF91-2424-4BD1-9133-E0E07AC1087E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a17ff5e4ec976fcf0c6be02e3fbc373d7ffd2f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946563"
---
# <span data-ttu-id="0b183-101">Get-AzureSqlDatabaseUsages</span><span class="sxs-lookup"><span data-stu-id="0b183-101">Get-AzureSqlDatabaseUsages</span></span>

## <span data-ttu-id="0b183-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0b183-102">SYNOPSIS</span></span>
<span data-ttu-id="0b183-103">Obtém o tamanho e o limite de tamanho de um banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="0b183-103">Gets the size and size limit of a SQL Database.</span></span>

## <span data-ttu-id="0b183-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b183-104">SYNTAX</span></span>

```
Get-AzureSqlDatabaseUsages -ServerName <String> -DatabaseName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b183-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0b183-105">DESCRIPTION</span></span>
<span data-ttu-id="0b183-106">O cmdlet **Get-AzureSqlDatabaseUsages** Obtém o tamanho atual e o limite de tamanho de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="0b183-106">The **Get-AzureSqlDatabaseUsages** cmdlet gets the current size and size limit of an Azure SQL Database.</span></span>

## <span data-ttu-id="0b183-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0b183-107">EXAMPLES</span></span>

### <span data-ttu-id="0b183-108">Exemplo 1: obter informações de uso de um banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="0b183-108">Example 1: Get usage information for a SQL Database</span></span>
```
PS C:\> Get-AzureSqlDatabaseUsages -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="0b183-109">Esse comando obtém as informações de tamanho e limite de tamanho para o banco de dados SQL chamado Database01 em Server01.</span><span class="sxs-lookup"><span data-stu-id="0b183-109">This command gets the size and size limit information for the SQL Database named Database01 on Server01.</span></span>

## <span data-ttu-id="0b183-110">OS</span><span class="sxs-lookup"><span data-stu-id="0b183-110">PARAMETERS</span></span>

### <span data-ttu-id="0b183-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0b183-111">-DatabaseName</span></span>
<span data-ttu-id="0b183-112">Especifica o nome do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="0b183-112">Specifies the name of the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b183-113">-Perfil</span><span class="sxs-lookup"><span data-stu-id="0b183-113">-Profile</span></span>
<span data-ttu-id="0b183-114">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="0b183-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0b183-115">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="0b183-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b183-116">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="0b183-116">-ServerName</span></span>
<span data-ttu-id="0b183-117">Especifica o nome do servidor que hospeda o banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="0b183-117">Specifies the name of the server that hosts the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b183-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b183-118">CommonParameters</span></span>
<span data-ttu-id="0b183-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b183-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b183-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b183-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b183-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0b183-121">INPUTS</span></span>

## <span data-ttu-id="0b183-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0b183-122">OUTPUTS</span></span>

## <span data-ttu-id="0b183-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0b183-123">NOTES</span></span>

## <span data-ttu-id="0b183-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b183-124">RELATED LINKS</span></span>

