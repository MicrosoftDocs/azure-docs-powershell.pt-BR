---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 7DBF937E-2D01-4356-9A5F-C5A4CB6D1A10
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebappslotconfigname
schema: 2.0.0
ms.openlocfilehash: 39c3ce693a1ee17a5b547c027ab9165388fe10f2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786040"
---
# <span data-ttu-id="5d3d0-101">Set-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="5d3d0-101">Set-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="5d3d0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5d3d0-102">SYNOPSIS</span></span>
<span data-ttu-id="5d3d0-103">Definir nomes de configuração do slot para aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="5d3d0-103">Set Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d3d0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5d3d0-104">SYNTAX</span></span>

### <span data-ttu-id="5d3d0-105">Eles</span><span class="sxs-lookup"><span data-stu-id="5d3d0-105">S1</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d3d0-106">S2</span><span class="sxs-lookup"><span data-stu-id="5d3d0-106">S2</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d3d0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5d3d0-107">DESCRIPTION</span></span>
<span data-ttu-id="5d3d0-108">O cmdlet **set-AzureRmWebAppSlotConfigName** marca as configurações do aplicativo e as cadeias de conexão como configurações do slot</span><span class="sxs-lookup"><span data-stu-id="5d3d0-108">The **Set-AzureRmWebAppSlotConfigName** cmdlet marks App Settings and Connection Strings as slot settings</span></span>

## <span data-ttu-id="5d3d0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5d3d0-109">EXAMPLES</span></span>

### <span data-ttu-id="5d3d0-110">1:</span><span class="sxs-lookup"><span data-stu-id="5d3d0-110">1:</span></span>
```
PS C:\> Set-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -RemoveAllAppSettingNames -RemoveAllConnectionStringNames
```

<span data-ttu-id="5d3d0-111">Esse comando Remove todas as configurações do aplicativo e cadeias de conexão do aplicativo Web ContosoWebApp associados ao grupo de recursos padrão-Web-Oesteus</span><span class="sxs-lookup"><span data-stu-id="5d3d0-111">This command removes all app settings and connection strings for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="5d3d0-112">OS</span><span class="sxs-lookup"><span data-stu-id="5d3d0-112">PARAMETERS</span></span>

### <span data-ttu-id="5d3d0-113">-AppSettingnames</span><span class="sxs-lookup"><span data-stu-id="5d3d0-113">-AppSettingNames</span></span>
<span data-ttu-id="5d3d0-114">Matriz de cadeias de nomes de configurações do aplicativo</span><span class="sxs-lookup"><span data-stu-id="5d3d0-114">App Settings Names String Array</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d3d0-115">-ConnectionStringnames</span><span class="sxs-lookup"><span data-stu-id="5d3d0-115">-ConnectionStringNames</span></span>
<span data-ttu-id="5d3d0-116">Matriz de cadeias de nomes de cadeia de conexão</span><span class="sxs-lookup"><span data-stu-id="5d3d0-116">Connection String Names String Array</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d3d0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d3d0-117">-DefaultProfile</span></span>
<span data-ttu-id="5d3d0-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5d3d0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d3d0-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="5d3d0-119">-Name</span></span>
<span data-ttu-id="5d3d0-120">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="5d3d0-120">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d3d0-121">-RemoveAllAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="5d3d0-121">-RemoveAllAppSettingNames</span></span>
<span data-ttu-id="5d3d0-122">Opção remover todos os nomes de configuração do aplicativo</span><span class="sxs-lookup"><span data-stu-id="5d3d0-122">Remove All App Setting Names Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3d0-123">-RemoveAllConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="5d3d0-123">-RemoveAllConnectionStringNames</span></span>
<span data-ttu-id="5d3d0-124">Opção remover todos os nomes de cadeia de conexão</span><span class="sxs-lookup"><span data-stu-id="5d3d0-124">Remove All Connection String Names Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3d0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d3d0-125">-ResourceGroupName</span></span>
<span data-ttu-id="5d3d0-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="5d3d0-126">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3d0-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="5d3d0-127">-WebApp</span></span>
<span data-ttu-id="5d3d0-128">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="5d3d0-128">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d3d0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d3d0-129">CommonParameters</span></span>
<span data-ttu-id="5d3d0-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d3d0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d3d0-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d3d0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d3d0-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5d3d0-132">INPUTS</span></span>

### <span data-ttu-id="5d3d0-133">Instalação</span><span class="sxs-lookup"><span data-stu-id="5d3d0-133">Site</span></span>
<span data-ttu-id="5d3d0-134">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="5d3d0-134">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="5d3d0-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5d3d0-135">OUTPUTS</span></span>

## <span data-ttu-id="5d3d0-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5d3d0-136">NOTES</span></span>

## <span data-ttu-id="5d3d0-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5d3d0-137">RELATED LINKS</span></span>

